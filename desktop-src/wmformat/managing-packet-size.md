---
title: Gestione delle dimensioni dei pacchetti
description: Gestione delle dimensioni dei pacchetti
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media Format SDK, gestione delle dimensioni dei pacchetti
- Windows Media Format SDK, dimensioni dei pacchetti
- profili, dimensioni dei pacchetti
- profili,gestione delle dimensioni dei pacchetti
- pacchetti, dimensioni
- packets,interfaccia IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b8755eccdcc0042532be4359cd51fce2ef379b51882e6cc4585c48c8769a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846713"
---
# <a name="managing-packet-size"></a>Gestione delle dimensioni dei pacchetti

Il writer è progettato per gestire internamente le dimensioni dei pacchetti. Tuttavia, potrebbero essere necessari requisiti specifici per l'applicazione che chiamano per un certo controllo manuale sulle dimensioni dei pacchetti nei file ASF che si scrivono. L Windows Media Format SDK offre due interfacce, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) e [**IWMPacketSize2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) che consentono di controllare le dimensioni massime e minime dei pacchetti.

Entrambe le interfacce delle dimensioni dei pacchetti vengono esposte nell'oggetto profilo. Sono disponibili anche per l'oggetto reader. Come per altre interfacce correlate al profilo, il lettore può accedere solo ai metodi di lettura.

Le dimensioni dei pacchetti hanno un effetto sulle prestazioni. In generale, minore è la dimensione del pacchetto, maggiore è la frammentazione dei dati all'interno di un file. Maggiore è la frammentazione di un file, meno efficiente sarà la ricostruirlo. In uno scenario di streaming, questa potrebbe non essere una considerazione importante, perché il processo di lettura di un file da un'origine Internet è in genere inefficiente. Quando si tratta di un file in locale, tuttavia, questa potrebbe essere una considerazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**Interfaccia IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




