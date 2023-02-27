# NAME

blockHashRead - Read a block hash file 

# DESCRIPTION

blockHashRead is a stand alone command line tool which converts a 
*block hash file* in to a list of hostnames. This way, a binary block 
hash file can be converted in to an ASCII list of host names, edited, 
and then converted back in to a binary block hash file with the 
**blockHashMake** utility. 

A block hash file uses a special binary format for storing a list of 
blocked host names. 

# USAGE

blockHashRead is invoked as follows:

```
blockHashRead --dump bigBlock.bin 
```

Replace "bigBlock.bin" with the filename for the block hash file. 

Doing this will output, on standard output, a list of host names in the 
block hash file. Each line will contain a single host name. When 
compiled for *NIX, the output will use *NIX line feeds; the Windows 
port of blockHashRead uses DOS line feeds. 

blockHashRead can be invoked with a single "--help" or "--version" 
command line argument (e.g. "blockHashRead --version") which will 
output the version number of blockHashRead and provide basic usage 
information. 

# HOST LIST FORMAT

After being invoked, blockHashRead writes a list of host names to the 
standard output. The format is a single host name per line of input, 
such as the following:

```
porn.example.com 
naughty.foo 
evil.host.invalid 
```

Each line is a host name. 

blockHashRead has no support for Punycode. Please use another program 
to convert international domain names with non-ASCII characters in to 
their non-punycode representation if seeing correct international 
domain names is desired. 

# LIMITATIONS

The block hash format that blockHashRead looks at is a 32-bit format, 
and the resulting block hash file should be under 2,147,483,648 bytes 
in size. This is a limitation of around 30 million host names. 

# LEGAL DISCLAIMERS

THIS SOFTWARE IS PROVIDED BY THE AUTHORS ''AS IS'' AND ANY EXPRESS OR 
IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED 
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE 
DISCLAIMED. IN NO EVENT SHALL THE AUTHORS OR CONTRIBUTORS BE LIABLE FOR 
ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL 
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS 
OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) 
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, 
STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING 
IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE 
POSSIBILITY OF SUCH DAMAGE. 

This is a project developed on a strictly volunteer, non-commercial 
basis. It has been developed outside the course of a commercial 
activity, developed entirely in the Americas (i.e. *outside of Europe*) 
and therefore is not subject to the restrictions or conditions of the 
proposed EU Cyber Resilience Act. Someone selling a product that uses 
any component of this may be subject to this act and may need to handle 
any and all necessary compliance. 

# AUTHORS

Sam Trenholme (https://www.samiam.org) is responsible for this program 
and man page.  

