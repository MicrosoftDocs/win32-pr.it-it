---
description: In alcuni casi potrebbe essere necessario determinare se l'applicazione è in esecuzione in un Tablet PC perché si desidera che le applicazioni possano sfruttare le funzionalità intrinseche di input penna, riconoscimento e penna.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Determinare se un PC è un Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316858"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a>Determinare se un PC è un Tablet PC

In alcuni casi potrebbe essere necessario determinare se l'applicazione è in esecuzione in un Tablet PC perché si desidera che le applicazioni possano sfruttare le funzionalità intrinseche di input penna, riconoscimento e penna. Per determinare se l'applicazione ha accesso alle funzionalità di Tablet PC, è possibile usare la chiamata all'API Windows GetSystemMetrics () come descritto in questo argomento.

## <a name="client-side-applications"></a>Applicazioni Client-Side

È possibile utilizzare le tecniche seguenti per determinare se il codice è in esecuzione in un Tablet PC.

-   [Uso di GetSystemMetrics (SM \_ TABLETPC)](/windows)
-   [Uso della presenza di file binari della piattaforma Tablet](#using-the-presence-of-tablet-platform-binaries)
-   [Applicazioni basate sul Web](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a>Uso di GetSystemMetrics (SM \_ TABLETPC)

### <a name="windows-xp-tablet-pc-edition"></a>Windows XP Tablet PC Edition

In Microsoft Windows XP Tablet PC Edition utilizzare la funzione GetSystemMetrics (SM \_ TABLETPC) per determinare se un computer è un Tablet PC. GetSystemMetrics (SM \_ TABLETPC) è progettato per restituire true in un computer in cui è in esecuzione Windows XP Tablet PC Edition.

### <a name="windows-vista"></a>Windows Vista

In Windows Vista non è più disponibile un Tablet PC SDK distinto. Il Windows SDK ora contiene una sezione denominata "Tablet PC and Touch Technology" e la logica di GetSystemMetrics (SM \_ TABLETPC) è stata modificata per riflettere questo problema. GetSystemMetrics (SM \_ TABLETPC) restituisce ora true se si verificano tutte le condizioni seguenti:

-   Nel sistema è presente un digitalizzatore integrato, ovvero Pen o touch.
-   Il componente facoltativo di Tablet PC è installato. Questo componente contiene funzionalità come il pannello input penna di Tablet PC e Windows Journal.
-   Il computer dispone di una licenza per l'utilizzo del componente facoltativo. Le versioni Premium di Windows Vista, ad esempio Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise e Windows Vista Ultimate, sono concesse in licenza per l'uso del componente facoltativo.
-   Il servizio di input di Tablet PC è in esecuzione. Il servizio di input di Tablet PC è un nuovo servizio di Windows Vista che controlla l'input di Tablet PC.

Con questa maggiore precisione, GetSystemMetrics (SM \_ TABLETPC) continua a essere il metodo consigliato per determinare se un computer che esegue Windows Vista è un Tablet PC.

### <a name="using-the-presence-of-tablet-platform-binaries"></a>Uso della presenza di file binari della piattaforma Tablet

In Windows XP Tablet PC Edition e Windows Vista è possibile cercare la presenza dei file binari di input penna, ad esempio inkobj.dll e Microsoft.Ink.dll, e utilizzare le funzionalità supportate, se presenti.

In Windows Vista, per impostazione predefinita, i file binari della piattaforma Tablet PC vengono installati in tutte le versioni client. Le funzionalità di input e Inking sono disponibili in tali versioni. Il riconoscimento è disponibile solo nelle versioni Premium di Windows Vista.

### <a name="web-based-applications"></a>Applicazioni Web-Based

In Windows Vista, la stringa dell'agente utente segnalata da Internet Explorer include "Tablet PC 2,0" Se, in base a GetSystemMetrics (SM \_ TABLETPC), il dispositivo è un Tablet PC.

In Windows XP Tablet PC Edition 2005, la stringa dell'agente utente include Tablet PC 1,7. La stringa dell'agente utente ha un aspetto simile al seguente:

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

Utilizzare questo valore per determinare se il computer client è un Tablet PC e supporta i controlli Inking basati sul Web.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
