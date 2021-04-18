---
title: Gestione del contenuto protetto nel provider di servizi
description: Gestione del contenuto protetto nel provider di servizi
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Media Gestione dispositivi, certificati
- Gestione dispositivi, certificati
- Guida per programmatori, certificati
- provider di servizi, certificati
- creazione di provider di servizi, certificati
- certificates
- Windows Media Gestione dispositivi, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- Guida per programmatori, contenuto protetto da DRM
- provider di servizi, contenuto protetto da DRM
- creazione di provider di servizi, contenuto protetto da DRM
- Contenuto protetto da DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298041"
---
# <a name="handling-protected-content-in-the-service-provider"></a>Gestione del contenuto protetto nel provider di servizi

È possibile creare un provider di servizi in grado di inviare contenuto protetto da DRM a un dispositivo basato su DRM (PDDRM) di dispositivi portatili, ma non è possibile creare un provider di servizi in grado di inviare contenuto protetto da DRM ai dispositivi basati su Windows Media DRM 10 per i dispositivi portatili. Questi dispositivi usano MTP e non è possibile creare un provider di servizi MTP personalizzato.

L'unico passaggio aggiuntivo che un provider di servizi deve eseguire per inviare materiale DRM a un dispositivo PDDRM consiste nell'ottenere una coppia di certificati/chiavi rilasciata da Microsoft. Vedere [gli strumenti per lo sviluppo](tools-for-development.md) per informazioni su dove ottenere questo certificato/chiave. Le licenze rilasciate a questi dispositivi saranno licenze semplificate che supportano solo la riproduzione semplice dei contenuti acquistati; non supporteranno le licenze in scadenza. Questa licenza verrà creata automaticamente dal provider di contenuti protetti (fornito da Microsoft per i file WMA/WMV) e archiviata nell'intestazione del file inviato al provider di servizi. Non sarà necessario eseguire alcun passaggio speciale per i file protetti.

Dopo l'invio del file protetto, Windows Media Gestione dispositivi chiamerà il provider di servizi per richiedere un file di archiviazione licenze speciale dal dispositivo. Windows Media Gestione dispositivi aggiungerà una copia della nuova licenza a questo file e lo restituirà al provider di servizi per inviare di nuovo il dispositivo. Tuttavia, anche se il provider di servizi non riesce a trovare o a restituire questo file, il dispositivo deve comunque essere in grado di riprodurre il file protetto usando la copia della licenza nell'intestazione del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> <dt>

[**Gestione del contenuto protetto**](handling-protected-content.md)
</dt> </dl>

 

 




