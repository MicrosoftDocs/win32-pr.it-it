---
description: In Windows Server 2003, WinHTTP viene implementato come assembly affiancato e deve essere collegato a tale scopo. Si noti che questa operazione non si applica a Windows Vista e versioni successive.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Uso di WinHTTP come assembly affiancato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751511"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Uso di WinHTTP come assembly affiancato

In Windows Server 2003, WinHTTP viene implementato come assembly affiancato e deve essere collegato a tale scopo. Si noti che questa operazione non si applica a Windows Vista e versioni successive.

## <a name="side-by-side-assemblies"></a>Assembly affiancati

A partire da Microsoft Windows XP, è stato fornito un meccanismo di assembly affiancati per controllare il collegamento della fase di esecuzione per evitare conflitti di controllo delle versioni delle librerie a collegamento dinamico (DLL). Per informazioni sugli assembly affiancati, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).

Per usare questo meccanismo per il collegamento a WinHTTP versione 5,1 in Windows Server 2003, un'applicazione deve incorporare un manifesto che specifichi WinHTTP come assembly dipendente. Per ulteriori informazioni su come eseguire questa operazione, vedere [utilizzo degli assembly affiancati](/windows/desktop/SbsCs/using-side-by-side-assemblies) .

## <a name="a-sample-winhttp-application-manifest"></a>Manifesto dell'applicazione WinHTTP di esempio

Il manifesto di esempio seguente illustra un manifesto dell'applicazione che può essere usato per il collegamento a WinHTTP.

Tutti gli attributi tranne "Type" di " <assembly> <assemblyIdentity> " devono essere modificati in modo appropriato per l'applicazione specifica. Lo stesso vale per il contenuto dell'elemento " &lt; Description &gt; ".

Assicurarsi inoltre che l'attributo "processorArchitecture" di " <dependentAssembly> <assemblyIdentity> " corrisponda all'attributo "ProcessorArchitecture" di " <assembly> <assemblyIdentity> ". Di seguito, ad esempio, entrambi sono impostati su "x86".

Tutti i valori non specifici dell'applicazione dovrebbero avere i moduli mostrati di seguito.

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

 

 
