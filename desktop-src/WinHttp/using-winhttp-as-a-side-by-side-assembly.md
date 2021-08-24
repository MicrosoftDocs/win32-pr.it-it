---
description: In Windows Server 2003, WinHTTP viene implementato come assembly side-by-side e deve essere collegato a come tale. Si noti che questo non si applica Windows Vista e versioni successive.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Uso di WinHTTP come assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c6312fb57f210e0324c1ae89bb785fd5b51bcb2b1ea4ba1a4959a3d0fd540
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614091"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Uso di WinHTTP come assembly side-by-side

In Windows Server 2003, WinHTTP viene implementato come assembly side-by-side e deve essere collegato a come tale. Si noti che questo non si applica Windows Vista e versioni successive.

## <a name="side-by-side-assemblies"></a>Assembly side-by-side

A partire da Microsoft Windows XP, è stato fornito un meccanismo di assembly side-by-side per controllare il collegamento in fase di esecuzione per evitare conflitti di controllo delle versioni della libreria a collegamento dinamico (DLL). Per informazioni sugli assembly side-by-side, vedere Informazioni sulle applicazioni isolate e sugli [assembly side-by-side](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).

Per usare questo meccanismo per il collegamento a WinHTTP versione 5.1 in Windows Server 2003, un'applicazione deve incorporare un manifesto che specifica WinHTTP come assembly dipendente. Per altre informazioni su come eseguire questa operazione, vedere Uso di assembly [side-by-side.](/windows/desktop/SbsCs/using-side-by-side-assemblies)

## <a name="a-sample-winhttp-application-manifest"></a>Manifesto dell'applicazione WinHTTP di esempio

Il manifesto di esempio seguente illustra un manifesto dell'applicazione che può essere usato per il collegamento a WinHTTP.

Tutti gli attributi ad eccezione di "type" di <assembly> <assemblyIdentity> " " devono essere modificati in base alle esigenze dell'applicazione specifica. Lo stesso vale per il contenuto dell'elemento " &lt; description &gt; ".

Assicurarsi inoltre che l'attributo "processorArchitecture" di " " corrisponda all'attributo <dependentAssembly> <assemblyIdentity> "processorArchitecture" di " <assembly> <assemblyIdentity> ". Di seguito, ad esempio, entrambi sono impostati su "x86".

Tutti i valori non specifici dell'applicazione devono assumere i formati illustrati di seguito.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
