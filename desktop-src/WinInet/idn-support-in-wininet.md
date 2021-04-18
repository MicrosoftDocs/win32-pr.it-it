---
title: Supporto IDN in WinINet
description: A partire da Windows Server 2008 e Windows Vista, la parte host dell'URL Unicode viene convertita in IDN (International Domain Name).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399588"
---
# <a name="idn-support-in-wininet"></a>Supporto IDN in WinINet

A partire da Windows Server 2008 e Windows Vista, la parte host dell'URL Unicode viene convertita in IDN (International Domain Name). Parti separate della codifica URL Unicode possono anche essere modificate dalle configurazioni impostate dall'applicazione. Le versioni ANSI dell'API WinINet continuano a inviare l'URL in transito come immesso dall'applicazione, ma le versioni Unicode di WinINet dell'API sono ora conformi allo standard IDN (RFC3490) per le codifiche URL.

Per impostazione predefinita, quando viene immesso un URL come parametro Unicode, la parte host, sia per il proxy che per le connessioni dirette, viene convertita in formato IDN. Nell'applicazione è possibile disabilitare la formattazione dell'host IDN impostando l'opzione **Internet \_ option \_ IDN** . La conversione dell'host IDN può essere abilitata solo per le connessioni dirette o proxy usando il **\_ flag Internet \_ IDN \_ Direct** o i flag del **proxy di Internet \_ flag \_ IDN \_** con l' **\_ opzione Internet \_ IDN**.

Nell'esempio di codice seguente viene illustrato come disabilitare la conversione host IDN sia per il proxy che per le connessioni dirette.

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

Se la formattazione dell'host IDN è disabilitata, l'applicazione ha la possibilità di specificare la tabella codici desiderata utilizzando l' **\_ opzione Internet \_ codepage**.

Nell'esempio di codice seguente viene illustrato come specificare la tabella codici giapponese.

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

La parte relativa al percorso dell'URL è codificata con UTF8 per impostazione predefinita e i segmenti rimanenti dell'URL, la query o il frammento, vengono convertiti nella tabella codici di sistema predefinita (CP \_ ACP).

Nell'esempio seguente viene illustrato come specificare la tabella codici della lingua coreana per la parte del percorso dell'URL.

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

La tabella seguente definisce le opzioni che supportano IDN. Per ulteriori informazioni, vedere l'argomento [flag di opzione](option-flags.md) .



| Opzione                            | Descrizione                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| opzione INTERNET (tabella \_ \_ codici)        | Questa opzione è impostata nella richiesta o nell'handle di connessione per specificare uno schema di codifica della tabella codici per la parte host dell'URL. Questa opzione viene ignorata se IDN è abilitato.                                                      |
| \_opzione Internet \_ percorso tabella codici \_  | Questa opzione è impostata nella richiesta oppure l'handle di connessione Abilita lo schema di codifica specificato per la parte del percorso dell'URL. Per impostazione predefinita, la parte del percorso dell'URL è con codifica UTF8.                                         |
| opzione INTERNET-tabella \_ \_ codici \_ aggiuntivi | L'impostazione di questa opzione sulla richiesta o sull'handle di connessione Abilita lo schema di codifica specificato per la parte aggiuntiva dell'URL. Per impostazione predefinita, la parte aggiuntiva dell'URL è codificata nella tabella codici di sistema predefinita (CP \_ ACP). |
| \_opzione Internet \_ IDN             | Questa opzione può essere utilizzata sulla richiesta o sull'handle di connessione per abilitare o disabilitare la conversione dell'host IDN. Quando IDN è disabilitato, WinINet usa la tabella codici di sistema predefinita per codificare la porzione host o Authority dell'URL.       |



 

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 