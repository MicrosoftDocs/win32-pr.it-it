---
title: ISRResGraphEx e IAttributes
description: ISRResGraphEx e IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659d7d4723bfc5145fb8abcc77043031a0e48e8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046572"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx e IAttributes

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Gli oggetti risultati restituiti dal motore devono supportare l'interfaccia ISRResGraphEx e l'interfaccia IAttributes. Il semplice supporto dell'interfaccia ISRResGraphEx è sufficiente per consentire all'editor di suoni di fornire informazioni di Word break, ma non fornisce il supporto necessario per le informazioni sui fonemi.

L'editor di suoni richiede che i motori supportino anche un attributo DWord speciale, **SRATTR \_ PHONESEG**. L'editor esegue una query sui motori per visualizzare l'interfaccia IAttributes e tenta di impostare **SRATTR \_ PHONESEG** su 1. Se la chiamata ha esito positivo, nell'editor di suoni si presuppone che i risultati del motore supporteranno la raccolta di informazioni relative alla segmentazione dei fonemi dall'oggetto results.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Quando un oggetto Results viene trasmesso all'editor audio, esegue una query sull'oggetto per la relativa implementazione di ISRResGraphEx. ISRResGraphEx contiene una funzione membro, DataGet, con firma del tipo

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Dove **dwID** è l'identificatore dell'oggetto Graph, **GATTRIB** è un GUID corrispondente all'attributo ricercato e **psData** è un puntatore a un oggetto SDATA contenente i dati restituiti. Il motore è responsabile dell'allocazione dei dati archiviati in **psData** tramite [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc). L'applicazione chiamante (in questo caso l'editor di suoni) è responsabile della liberazione tramite [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) al termine dell'operazione.

DataGet è necessario per riconoscere tre GUID predefiniti, elencati nella documentazione di SAPI. Un motore che restituisce un codice di esito positivo alla chiamata a **DWORDSet (SRATTR \_ PHONESEG, 1)** è necessario anche per riconoscere un GUID specifico, **SRGARC \_ PHONEMESEGMENTATION**, quando viene chiamato con un **dwID** che corrisponde a un bordo del grafico.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Quando la chiamata restituisce, **psData** deve puntare a una matrice di una struttura con allineamento DWORD di tipo **PHONESEG**, definita da:

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

dove **qwStartTime** e **qwEndTime** puntano all'inizio e alla fine di ogni fonema che costituisce la parola coperta dal perimetro e **aPhones** è una matrice di caratteri Unicode corrispondente alla rappresentazione IPA del telefono, che è stata prodotta in questo segmento. In alcune lingue sono presenti fonemi digitati con più di un fonema IPA. In inglese, ad esempio, il suono "Long I" nella parola "Live" è in realtà un dittongo, costituito da due fonemi più semplici concatenati. La matrice **aPhones** deve essere con terminazione zero e riempita alla fine per rendere ogni struttura **SRPHONESEG** nella matrice una lunghezza pari a un multiplo di quattro byte.

Si supponga, ad esempio, che la parola pronunciata in Arc 4 fosse "made". La chiamata a DataGet (4, **SRGARC \_ PHONEMESEGMENTATION**, &SD) potrebbe restituire una matrice di tre segmenti fonema,/m/che esegue da **qwStartTime**= 328434 byte **a qwEndTime**= 330354 byte,/1e/in esecuzione da **qwStartTime**= 330354 byte a **qwEndTime**= 344114 byte e/d/in esecuzione da **qwStartTime**= 344114 byte a **qwEndTime**= 347314 byte. Questi vengono presentati come una matrice compressa di tre strutture **SRPHONESEG** di dimensioni rispettivamente 28, 32 e 28 byte. Si noti che è presente una spaziatura interna alla fine della struttura **SRPHONESEG** intermedia, in modo che l'elemento successivo nella matrice inizi a un limite di 4 byte.

SAPI 4,0 SDK include uno strumento (SRFunc) per il test della conformità con la specifica SAPI 4,0. Incluso in tale strumento è un test di conformità a questo set di interfacce. Il codice sorgente per tale strumento è un buon punto di partenza per comprendere il modo in cui queste interfacce interagiranno con l'editor di suoni e per eseguire il debug delle interfacce durante lo sviluppo.

 

 