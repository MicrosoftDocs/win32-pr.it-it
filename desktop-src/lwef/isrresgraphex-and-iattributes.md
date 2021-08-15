---
title: ISRResGraphEx e IAttributes
description: ISRResGraphEx e IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f5e08b77b917e4630afcaeb8baed5aac4e13c20a1ed289418681abbbdca20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748997"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx e IAttributes

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Gli oggetti risultati restituiti dal motore devono supportare l'interfaccia ISRResGraphEx e l'interfaccia IAttributes. Il semplice supporto dell'interfaccia ISRResGraphEx è sufficiente per consentire all'editor audio di fornire informazioni sulle interruzioni di parola, ma non fornisce il supporto necessario per le informazioni sul fonema.

L'editor audio richiede che i motori supportino anche un attributo DWord speciale, **SRATTR \_ PHONESEG.** L'editor esegue una query sui motori per visualizzare l'interfaccia IAttributes e tenta di impostare **SRATTR \_ PHONESEG** su 1. Se la chiamata ha esito positivo, l'editor audio presuppone che i risultati del motore supportino la raccolta di informazioni sulla segmentazione del fonema dall'oggetto risultati.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Quando un oggetto risultati viene trasmesso all'editor audio, esegue una query su tale oggetto per l'implementazione di ISRResGraphEx. ISRResGraphEx contiene una funzione membro, DataGet, con firma del tipo

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Dove **dwID è** l'identificatore dell'oggetto grafico, **gAttrib** è un GUID corrispondente all'attributo cercato e **psData** è un puntatore a un oggetto SDATA contenente i dati restituiti. Il motore è responsabile dell'allocazione dei dati archiviati in **psData** tramite [**CoTaskMemAlloc.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) L'applicazione chiamante (in questo caso l'editor audio) è responsabile della sua liberazione tramite [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) al termine dell'operazione.

DataGet è necessario per riconoscere tre GUID predefiniti, elencati nella documentazione SAPI. Un motore che restituisce un codice di esito positivo alla chiamata a **DWORDSet(SRATTR \_ PHONESEG, 1)** è necessario anche per riconoscere un GUID specifico, **SRGARC \_ PHONEMESEGMENTATION,** quando viene chiamato con **un dwID** che corrisponde a un bordo nel grafico.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Quando la chiamata viene restituita, **psData** deve puntare a una matrice di struttura allineata a DWORD di tipo **PHONESEG,** definita da:

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

dove **qwStartTime** e **qwEndTime** puntano all'inizio e alla fine di ogni fonema che rappresenta la parola coperta dal bordo e **aPhones** è una matrice di caratteri Unicode corrispondente alla rappresentazione IPA del telefono, che sono stati prodotti in questo segmento. In alcune lingue sono presenti fonemi digitati con più di un fonema IPA. In inglese, ad esempio, il suono "long I" nella parola "live" è in realtà un diphthong, costituito da due fonemi più semplici concatenati. La **matrice aPhones** deve essere con terminazione zero e riempita alla fine per rendere ogni **struttura SRPHONESEG** nella matrice un multiplo pari di quattro byte.

Si supponga, ad esempio, che la parola parlata sull'arco 4 sia stata "fatta". Quindi la chiamata a DataGet(4, **SRGARC \_ PHONEMESEGMENTATION**, &sd) potrebbe restituire una matrice di tre segmenti di fonema, /m/ in esecuzione da **qwStartTime**=328434 bytes a **qwEndTime**=330354 bytes, /1e/ in esecuzione da **qwStartTime**=330354 bytes a **qwEndTime**=344114 bytes e /d/ in esecuzione da **qwStartTime**=344114 bytes a **qwEndTime**=347314 bytes. Queste vengono presentate come matrice compressa di tre strutture **SRPHONESEG** di dimensioni di 28, 32 e 28 byte, rispettivamente. Si noti che è presente una spaziatura interna alla fine della struttura **SRPHONESEG** centrale, in modo che l'elemento successivo nella matrice inizi in corrispondenza di un limite di 4 byte.

SAPI 4.0 SDK include uno strumento (SRFunc) per testare la conformità con la specifica SAPI 4.0. In questo strumento è incluso un test per la conformità con questo set di interfacce. Il codice sorgente per tale strumento è un buon punto di partenza per comprendere in che modo queste interfacce interagiscono con l'editor audio ed eseguire il debug delle interfacce durante lo sviluppo.

 

 