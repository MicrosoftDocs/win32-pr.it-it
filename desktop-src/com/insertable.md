---
title: Insertable (chiave CLSID)
description: Indica che gli oggetti di questa classe devono essere visualizzati nella casella di riepilogo della finestra di dialogo Inserisci oggetto quando vengono utilizzati dalle applicazioni contenitore COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Chiave del registro di sistema Insertable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047750"
---
# <a name="insertable-clsid-key"></a>Insertable (chiave CLSID)

Indica che gli oggetti di questa classe devono essere visualizzati nella casella di riepilogo della finestra di dialogo **Inserisci oggetto** quando vengono utilizzati dalle applicazioni contenitore com.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Commenti

Questa chiave è una voce obbligatoria per le applicazioni COM a 32 bit i cui oggetti possono essere inseriti in applicazioni a 16 bit esistenti. Le applicazioni a 16 bit esistenti esaminano il registro di sistema per questa chiave, che informa l'applicazione che il server supporta l'incorporamento. Se la chiave **Insertable** esiste, le applicazioni a 16 bit possono anche tentare di verificare che il server esista nel computer. le applicazioni a 16 bit recuperano in genere il valore della chiave [**LocalServer**](localserver.md) dalla classe e verificano se è un file valido nel sistema. Pertanto, per poter inserire un'applicazione a 32 bit da un'applicazione a 16 bit, è necessario che l'applicazione a 32 bit registri la sottochiave **LocalServer** oltre alla registrazione di [**LocalServer32**](localserver32.md).

Usato con i controlli, questa voce indica che un oggetto può fungere solo da oggetto incorporato sul posto senza funzionalità di controllo particolari. Gli oggetti che dispongono di questa chiave vengono visualizzati nella finestra di dialogo **Inserisci oggetto** per il relativo contenitore. Quando viene usato con i controlli, questa voce indica anche che il controllo è stato testato con contenitori non di controllo. Anche questa voce è facoltativa e può essere omessa quando un controllo non è progettato per funzionare con i contenitori meno recenti che non sono in grado di riconoscere i controlli.

> [!Note]  
> Questa chiave non è presente per classi interne come le classi moniker.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




