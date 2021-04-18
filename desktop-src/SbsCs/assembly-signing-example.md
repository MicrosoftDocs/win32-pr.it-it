---
description: Nell'esempio seguente viene illustrato come generare un assembly affiancato firmato costituito dal manifesto dell'assembly, dal catalogo di verifica e dai file di assembly.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Esempio di firma degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322040"
---
# <a name="assembly-signing-example"></a>Esempio di firma degli assembly

Nell'esempio seguente viene illustrato come generare un assembly affiancato firmato costituito dal manifesto dell'assembly, dal catalogo di verifica e dai file di assembly. Gli assembly side-by-side condivisi devono essere firmati. Il sistema operativo verifica la firma dell'assembly prima di installare un assembly condiviso nell'archivio side-by-side globale (WinSxS). In questo modo è difficile eseguire lo spoofing dell'editore dell'assembly affiancato.

Si noti che la modifica dei file di assembly o del contenuto del manifesto dopo la generazione del catalogo degli assembly invalida il catalogo e l'assembly. Se è necessario aggiornare i file di assembly o il manifesto dopo la creazione e la firma del catalogo, è necessario firmare di nuovo l'assembly e generare un nuovo catalogo.

Iniziare con i file di assembly, il manifesto dell'assembly e il file del certificato che si userà per firmare l'assembly. Il file del certificato deve avere una lunghezza di 2048 bit o superiore. Non è necessario usare un certificato attendibile. Il certificato viene usato solo per verificare che l'assembly non sia stato danneggiato.

Eseguire l'utilità di [Pktextract.exe](pktextract-exe.md) fornita nel Software Development Kit (SDK) di Microsoft Windows per estrarre il token di chiave pubblica dal file del certificato. Per il corretto funzionamento di Pktextract, il file del certificato deve essere presente nella stessa directory dell'utilità. Usare il valore del token di chiave pubblica Estratto per aggiornare l'attributo **PublicKeyToken** dell'elemento **assemblyIdentity** nel file manifesto.

Di seguito è riportato un esempio di un file manifesto denominato MySampleAssembly. manifest. L'assembly MySampleAssembly contiene un solo file, MYFILE.DLL. Si noti che il valore dell'attributo **PublicKeyToken** dell'elemento **assemblyIdentity** è stato aggiornato con il valore del token di chiave pubblica.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

Eseguire quindi l'utilità [Mt.exe](mt-exe.md) fornita nel Windows SDK. I file di assembly devono trovarsi nella stessa directory del manifesto. In questo esempio si tratta della directory MySampleAssembly. Chiamare Mt.exe per l'esempio come indicato di seguito:

**c: \\ MySampleAssembly>mt.exe-manifest MySampleAssembly. manifest-hashupdate-makecdfs**

Ecco come appare il manifesto di esempio dopo l'esecuzione Mt.exe. Si noti che l'esecuzione di Mt.exe con l'opzione hashupdate aggiunge l'hash SHA-1 del file. Non modificare questo valore.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

L'esecuzione di Mt.exe con l'opzione-makecdfs genera un file denominato MySampleAssembly. manifest. CDF che descrive il contenuto del catalogo di sicurezza che verrà usato per convalidare il manifesto.

Il passaggio successivo consiste nell'eseguire Makecat.exe su questo. CDF per creare il catalogo di sicurezza per l'assembly. La chiamata a Makecat.exe per questo esempio apparirà come segue:

**c: \\ MySampleAssembly>MakeCat MySampleAssembly. manifest. CDF**

Il passaggio finale consiste nell'eseguire SignTool.exe per firmare il file di catalogo con il certificato. Deve corrispondere allo stesso certificato usato in precedenza per generare il token di chiave pubblica. Per ulteriori informazioni su SignTool.exe vedere l'argomento [**SignTool**](../seccrypto/signtool.md) . La chiamata a **SignTool** per l'esempio apparirà come segue:

**c: \\ MySampleAssembly>signtool sign/f \<fullpath> MyCompany. pfx/du https: \/ /www.mycompany.com/MySampleAssembly/t https: \/ /timestamp.DigiCert.com MySampleAssembly.cat**

Se si dispone di un certificato digitale autenticato e l'autorità di certificazione usa il formato di file PVK per archiviare la chiave privata, è possibile usare l'utilità di importazione dei file di certificato digitale PVK (pvkimprt.exe) per importare la chiave nel provider del servizio di crittografia (CSP). Questa utilità consente di esportare nel formato standard del settore PFX/P12. Per ulteriori informazioni sull'utilità di importazione dei file di certificato digitale PVK, vedere la sezione relativa alle risorse di distribuzione in MSDN Library o contattare l'autorità di certificazione. Potrebbe essere possibile ottenere pvkimprt.exe da https://office.microsoft.com/downloads/2000/pvkimprt.aspx .

Vedere anche [creazione di file e cataloghi firmati](creating-signed-files-and-catalogs.md).

 

 
