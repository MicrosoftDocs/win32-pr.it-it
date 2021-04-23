---
description: La classe FOURCCMap fornisce la conversione tra sottotipi di supporti GUID e tag multimediali FOURCC a 32 bit di vecchio stile.
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
ms.openlocfilehash: b9254986bebadeffafaa832817f59194bfc58e12
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908859"
---
# <a name="fourccmap-class"></a>Classe FOURCCMap

![Gerarchia di classi fourccmap](images/fourcc01.png)

La **classe FOURCCMap** fornisce la conversione tra **sottotipi di** supporti GUID e tag multimediali **FOURCC** a 32 bit di vecchio stile. Nelle API multimediali windows originali, i tipi di supporti sono stati contrassegnati con valori a 32 bit creati da quattro caratteri a 8 bit ed erano noti come **FOURCC.** I tipi di supporti DirectShow hanno **GUID** per il sottotipo, in parte perché sono più semplici da creare (la creazione di un nuovo **FOURCC** richiede la registrazione con Microsoft). Poiché **fourcc** s sono univoci, è stato reso possibile un mapping uno-a-uno allocando un intervallo di 4.000 milioni di **GUID** che rappresentano **FOURCC** s. Questo intervallo è tutto **GUID** nel formato:

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Questa classe semplifica la conversione **tra GUID** e **FOURCC** s. Questo è solo per la compatibilità. È consigliabile che tutti i nuovi sottotipi multimediali siano rappresentati da **GUID** creati da Guidgen.exe o da uno strumento simile e non tramite il mapping **di FOURCC** s.

L'oggetto è derivato da **un GUID**, senza membri dati aggiuntivi e può essere eseguito il cast a un **GUID**. L'oggetto può essere passato a **FOURCC** in fase di costruzione. Il costruttore predefinito inizializzerà **FOURCC** su zero.

I [**metodi GetFOURCC**](fourccmap-getfourcc.md) e [**SetFOURCC**](fourccmap-setfourcc.md) non verificano che le parti fisse del **GUID** corrispondano all'intervallo **FOURCC.** Pertanto, se si esegue il cast di un puntatore a un **GUID** in un puntatore a **fourcc** e quindi si imposta o si ottiene il campo **FOURCC,** è necessario verificare separatamente che il **GUID** sia compreso nell'intervallo **FOURCC.**

## <a name="member-functions"></a>Funzioni di membro



| Label | Valore |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | Metodo del costruttore.                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | Recupera **l'oggetto FOURCC** da un **oggetto FOURCCMap.**    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | Imposta la **parte FOURCC** dell'oggetto **FOURCCMap.** |



 

 

 



