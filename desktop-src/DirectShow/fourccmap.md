---
description: La classe FOURCCMap consente la conversione tra sottotipi di supporti GUID e tag multimediali FOURCC a 32 bit in stile precedente.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: Classe FOURCCMap
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: a0ba22ce288535a8d940a5f70275f0152ffa559090d820b77df06ed3d1a9178d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043267"
---
# <a name="fourccmap-class"></a>Classe FOURCCMap

![Gerarchia di classi fourccmap](images/fourcc01.png)

La **classe FOURCCMap consente** la conversione tra sottotipi di supporti **GUID** e tag multimediali **FOURCC** a 32 bit in stile precedente. Nella versione originale Windows api multimediali, i tipi di supporti sono stati contrassegnati con valori a 32 bit creati da quattro caratteri a 8 bit ed erano noti come **FOURCC** s. DirectShow tipi di supporti hanno **GUID** per il sottotipo, in parte perché sono più semplici da creare (la creazione di un nuovo **FOURCC** richiede la registrazione con Microsoft). Poiché **fourcc** s sono univoci, è stato reso possibile un mapping uno-a-uno allocando un intervallo di 4.000 milioni **di GUID** che rappresentano **FOURCC** s. Questo intervallo è tutto **GUID** nel formato:

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Questa classe semplifica la conversione **tra GUID** e **FOURCC** s. Solo per motivi di compatibilità. È consigliabile che tutti i nuovi sottotipi di supporti siano rappresentati da **GUID** creati da Guidgen.exe o da uno strumento simile e non tramite il mapping **di FOURCC.**

L'oggetto è derivato da **un GUID**, senza membri dati aggiuntivi, ed è possibile eseguire il cast a un **GUID**. L'oggetto può essere passato a **FOURCC in** fase di costruzione. Il costruttore predefinito inizializzerà **FOURCC** su zero.

I [**metodi GetFOURCC**](fourccmap-getfourcc.md) [**e SetFOURCC**](fourccmap-setfourcc.md) non verificano che le parti fisse del **GUID** corrispondano all'intervallo **FOURCC.** Pertanto, se si esegue il cast di un puntatore a un **GUID** in un puntatore a **fourCC** e quindi si imposta o si ottiene il campo **FOURCC,** è necessario verificare separatamente che il **GUID** sia compreso nell'intervallo **FOURCC.**

## <a name="member-functions"></a>Funzioni di membro



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | Metodo del costruttore.                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | Recupera **l'oggetto FOURCC** da un **oggetto FOURCCMap.**    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | Imposta la **parte FOURCC** dell'oggetto **FOURCCMap.** |



 

 

 



