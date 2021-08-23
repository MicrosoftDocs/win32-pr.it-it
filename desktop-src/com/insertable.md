---
title: Insertable (chiave CLSID)
description: Indica che gli oggetti di questa classe devono essere visualizzati nella casella di riepilogo della finestra di dialogo Inserisci oggetto quando vengono utilizzati dalle applicazioni contenitore COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Com della chiave del Registro di sistema inseribile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c2d5d781545be05821b801b9e16048d2a097927890a63ead8f602c34d95613
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678591"
---
# <a name="insertable-clsid-key"></a>Insertable (chiave CLSID)

Indica che gli oggetti di questa classe devono essere visualizzati nella **casella** di riepilogo della finestra di dialogo Inserisci oggetto quando vengono utilizzati dalle applicazioni contenitore COM.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Commenti

Questa chiave è una voce obbligatoria per le applicazioni COM a 32 bit i cui oggetti possono essere inseriti in applicazioni a 16 bit esistenti. Le applicazioni a 16 bit esistenti cercano questa chiave nel Registro di sistema, che informa l'applicazione che il server supporta le incorporamenti. Se la **chiave inseribile** esiste, le applicazioni a 16 bit possono anche tentare di verificare che il server esista nel computer. Le applicazioni a 16 bit recuperano in genere il valore della chiave [**LocalServer**](localserver.md) dalla classe e verificano se si tratta di un file valido nel sistema. Pertanto, per un'applicazione a 32 bit che può essere inserita da un'applicazione a 16 bit, l'applicazione a 32 bit deve registrare la sottochiave **LocalServer** oltre a [**registrare LocalServer32.**](localserver32.md)

Utilizzata con i controlli , questa voce indica che un oggetto può fungere solo da oggetto incorporato sul posto senza funzionalità di controllo speciali. Gli oggetti con questa chiave vengono visualizzati nella **finestra di dialogo** Inserisci oggetto per il relativo contenitore. Se usata con i controlli , questa voce indica anche che il controllo è stato testato con contenitori non di controllo. Questa voce è facoltativa e può essere omessa quando un controllo non è progettato per funzionare con contenitori meno recenti che non comprendono i controlli.

> [!Note]  
> Questa chiave non è presente per le classi interne come le classi moniker.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




