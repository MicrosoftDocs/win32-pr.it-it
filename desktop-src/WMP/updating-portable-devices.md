---
title: Aggiornamento di dispositivi portatili
description: Aggiornamento di dispositivi portatili
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player Online Stores, aggiornamento di dispositivi portatili
- archivi online, aggiornamento di dispositivi portatili
- digitare 1 negozi online, aggiornamento di dispositivi portatili
- Windows Media Player Online Stores, dispositivi portatili
- negozi online, dispositivi portatili
- digitare 1 negozi online, dispositivi portatili
- aggiornamento di dispositivi portatili
- dispositivi portatili, aggiornamento
- dispositivi portatili, Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336265"
---
# <a name="updating-portable-devices"></a>Aggiornamento di dispositivi portatili

Windows Media Player consente agli utenti di sincronizzare il contenuto multimediale digitale con i dispositivi portatili. Questo può includere contenuto musicale acquistato o affittato da un negozio online. In alcune circostanze, i provider di archivio online potrebbero voler scrivere codice per lavorare su un dispositivo portatile connesso nell'ambito della gestione del contenuto fornito dallo Store. Per concedere al plug-in Online Store la possibilità di usare un dispositivo connesso, Windows Media Player chiama [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) e fornisce il nome canonico del dispositivo portatile. Se il codice del plug-in determina che alcune operazioni devono essere eseguite con il dispositivo connesso, deve restituire immediatamente S \_ OK dalla chiamata a **UpdateDevice** prima di procedere con l'operazione. Se non è necessario eseguire alcuna operazione, il plug-in deve restituire un codice di errore.

Al termine dell'uso del dispositivo da parte del plug-in, è necessario chiamare [IWMPContentPartnerCallback:: UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) per notificare a Windows Media Player che il dispositivo è disponibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi di tipo 1 online**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




