---
title: Co-Branding negozi online
description: Co-Branding negozi online
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player Online Stores, co-branding
- negozi online, co-branding
- digitare 1 negozi online, co-branding
- digitare 2 negozi online, co-branding
- negozi online di co-branding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298213"
---
# <a name="co-branding-online-stores"></a>Co-Branding negozi online

I personal computer OEM che non operano in un Music Store possono coesistere con i provider di negozio online. Il programma di installazione di Windows Media Player supporta il parametro della riga di comando ServiceExtra per consentire agli OEM hardware di impostare un attributo personalizzato che può essere utilizzato dall'archivio online per identificare quale OEM ha installato l'archivio online iniziale.

Ad esempio, se un produttore di computer denominato Fabrikam vuole impostare l'archivio online iniziale su Proseware Music Store, potrebbe usare la riga di comando seguente per installare Windows Media Player 10:


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



Quando Windows Media Player viene installato in questo modo, il lettore aggiunge la stringa ServiceExtra ogni volta che viene aperto il servizio proseware. Nell'esempio seguente viene illustrato l'URL che Windows Media Player invierà al servizio Proseware per recuperare il documento ServiceInfo:


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



L'archivio online di Proseware può quindi usare la stringa di query per determinare quale Windows OEM installato Media Player e restituire un documento ServiceInfo generato in modo dinamico che punti alla versione co-branding del negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Configurare i parametri della riga di comando per i negozi online**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




