---
title: Gestione delle dimensioni dei pacchetti
description: Gestione delle dimensioni dei pacchetti
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media Format SDK, gestione delle dimensioni dei pacchetti
- Windows Media Format SDK, dimensioni dei pacchetti
- profili, dimensioni dei pacchetti
- profili, gestione delle dimensioni dei pacchetti
- pacchetti, dimensioni
- pacchetti, interfaccia IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398761"
---
# <a name="managing-packet-size"></a>Gestione delle dimensioni dei pacchetti

Il writer è progettato per gestire le dimensioni dei pacchetti internamente. Tuttavia, potrebbero essere presenti requisiti specifici per l'applicazione che richiedono un controllo manuale sulle dimensioni dei pacchetti nei file ASF scritti. Windows Media Format SDK fornisce due interfacce, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) e [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , che consentono di controllare le dimensioni massime e minime dei pacchetti.

Entrambe le interfacce delle dimensioni del pacchetto sono esposte nell'oggetto profilo. Sono disponibili anche per l'oggetto Reader. Come per le altre interfacce correlate al profilo, il lettore può accedere solo ai metodi di lettura.

Le dimensioni dei pacchetti hanno un effetto sulle prestazioni. In generale, minore è la dimensione del pacchetto, più frammenti sono i dati all'interno di un file. Maggiore è la frammentazione di un file, minore sarà il modo più efficiente per ricostruirlo. In uno scenario di streaming, questo potrebbe non essere una considerazione importante, perché il processo di lettura di un file da un'origine Internet è in genere inefficiente. Quando si tratta di un file localmente, questo potrebbe essere una considerazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**Interfaccia IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




