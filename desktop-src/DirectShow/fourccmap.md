---
description: La classe FOURCCMap fornisce la conversione tra sottotipi di supporto GUID e tag per supporti FOURCC a 32 bit obsoleti.
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
ms.openlocfilehash: fd30a0f04d98b4c6ba4b7716a1a72d527873dbff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124551"
---
# <a name="fourccmap-class"></a>Classe FOURCCMap

![gerarchia di classi fourccmap](images/fourcc01.png)

La classe **FOURCCMap** fornisce la conversione tra sottotipi di supporto **GUID** e tag per supporti **fourcc** a 32 bit obsoleti. Nelle API multimediali di Windows originali, i tipi di supporto sono stati contrassegnati con i valori a 32 bit creati da caratteri a 4 8 bit ed erano noti come **fourcc** s. I tipi di supporto DirectShow hanno **GUID** per il sottotipo, in parte perché sono più semplici da creare (la creazione di un nuovo **fourcc** richiede la registrazione con Microsoft). Poiché i **fourcc** sono univoci, è possibile eseguire un mapping uno-a-uno allocando un intervallo di 4 miliardi **GUID** che rappresenta **fourcc** s. Questo intervallo è costituito da tutti i **GUID** nel formato:

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Questa classe semplifica la conversione tra **GUID** s e **fourcc** s. Questa operazione è solo per compatibilità. È consigliabile che tutti i nuovi sottotipi di supporti siano rappresentati da **GUID** s creati da Guidgen.exe o da uno strumento simile e non dal mapping di **fourcc** s.

L'oggetto è derivato da un **GUID**, senza membri dati aggiuntivi, ed è possibile eseguirne il cast in un **GUID**. È possibile passare un **fourcc** all'oggetto in fase di costruzione. Il costruttore predefinito inizializza **fourcc** su zero.

I metodi [**GetFOURCC**](fourccmap-getfourcc.md) e [**SetFOURCC**](fourccmap-setfourcc.md) non verificano che le parti fisse del **GUID** corrispondano all'intervallo di **fourcc** . Pertanto, se si esegue il cast di un puntatore a un **GUID** in un puntatore a un **fourcc** e quindi si imposta o si ottiene il campo **fourcc** , è necessario controllare separatamente che il **GUID** sia compreso nell'intervallo di **fourcc** .

## <a name="member-functions"></a>Funzioni di membro



|                                          |                                                          |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | Metodo del costruttore.                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | Recupera **fourcc** da un oggetto **FOURCCMap** .    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | Imposta la parte **fourcc** dell'oggetto **FOURCCMap** . |



 

 

 



