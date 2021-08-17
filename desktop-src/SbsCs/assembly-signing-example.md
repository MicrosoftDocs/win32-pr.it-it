---
description: Nell'esempio seguente viene illustrato come generare un assembly side-by-side firmato costituito dal manifesto dell'assembly, dal catalogo di verifica e dai file di assembly.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Esempio di firma degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896da43b846edfd09348c6515fbf5e44fdd45dd2911b9fcdcf25e99f63fb6ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142464"
---
# <a name="assembly-signing-example"></a>Esempio di firma degli assembly

Nell'esempio seguente viene illustrato come generare un assembly side-by-side firmato costituito dal manifesto dell'assembly, dal catalogo di verifica e dai file di assembly. Gli assembly side-by-side condivisi devono essere firmati. Il sistema operativo verifica la firma dell'assembly prima di installare un assembly condiviso nell'archivio side-by-side globale (WinSxS). Ciò rende difficile lo spoofing dell'editore dell'assembly side-by-side.

Si noti che la modifica dei file di assembly o del contenuto del manifesto dopo la generazione del catalogo degli assembly invalida il catalogo e l'assembly. Se è necessario aggiornare i file di assembly o il manifesto dopo aver creato e firmato il catalogo, è necessario firmare nuovamente l'assembly e generare un nuovo catalogo.

Iniziare con i file di assembly, il manifesto dell'assembly e il file di certificato che verrà utilizzato per firmare l'assembly. Il file del certificato deve essere di 2048 bit o superiore. Non è necessario usare un certificato attendibile. Il certificato viene usato solo per verificare che l'assembly non sia stato danneggiato.

Eseguire [lPktextract.exeutilità](pktextract-exe.md) fornita in Microsoft Windows Software Development Kit (SDK) per estrarre il token di chiave pubblica dal file del certificato. Per il corretto funzionamento di Pktextract, il file del certificato deve essere presente nella stessa directory dell'utilità. Usare il valore del token di chiave pubblica estratto per aggiornare **l'attributo publicKeyToken** dell'elemento **assemblyIdentity** nel file manifesto.

Di seguito è riportato un esempio di file manifesto denominato MySampleAssembly.manifest. L'assembly MySampleAssembly contiene un solo file, MYFILE.DLL. Si noti che il valore **dell'attributo publicKeyToken** dell'elemento **assemblyIdentity** è stato aggiornato con il valore del token di chiave pubblica.

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

Eseguire quindi [l'Mt.exe](mt-exe.md) disponibile nell'SDK Windows. I file di assembly devono trovarsi nella stessa directory del manifesto. In questo esempio si tratta della directory MySampleAssembly. Chiamare Mt.exe per l'esempio come segue:

**c: \\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**

Ecco l'aspetto del manifesto di esempio dopo l'esecuzione Mt.exe. Si noti che lMt.exe con l'opzione hashupdate aggiunge l'hash SHA-1 del file. Non modificare questo valore.

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

LMt.exe con l'opzione -makecdfs genera un file denominato MySampleAssembly.manifest.cdf che descrive il contenuto del catalogo di sicurezza che verrà usato per convalidare il manifesto.

Il passaggio successivo consiste nell'eseguire Makecat.exe su questo file con estensione cdf per creare il catalogo di sicurezza per l'assembly. La chiamata a Makecat.exe per questo esempio verrà visualizzata come segue:

**c: \\ MySampleAssembly>makecat MySampleAssembly.manifest.cdf**

Il passaggio finale consiste nell'eseguire SignTool.exe firmare il file di catalogo con il certificato. Deve essere lo stesso certificato usato nel precedente per generare il token di chiave pubblica. Per altre informazioni sui SignTool.exe vedere [**l'argomento SignTool.**](../seccrypto/signtool.md) La chiamata a **SignTool per** l'esempio verrà visualizzata come segue:

**c: \\ MySampleAssembly>signtool sign /f \<fullpath> mycompany.pfx /du https: \/ /www.mycompany.com/MySampleAssembly /t https: \/ /timestamp.digicert.com MySampleAssembly.cat**

Se si dispone di un certificato digitale autenticato e l'autorità di certificazione usa il formato di file PVK per archiviare la chiave privata, è possibile usare l'utilità di importazione dei file dei certificati digitali PVK (pvkimprt.exe) per importare la chiave nel provider del servizio di crittografia (CSP). Questa utilità consente di esportare nel formato standard del settore PFX/P12. Per altre informazioni sull'utilità di importazione file di certificati digitali PVK, vedere la sezione Risorse di distribuzione di MSDN Library o contattare l'autorità di certificazione. Potrebbe essere possibile ottenere pvkimprt.exe da https://office.microsoft.com/downloads/2000/pvkimprt.aspx .

Vedere anche Creazione [di file e cataloghi firmati.](creating-signed-files-and-catalogs.md)

 

 
