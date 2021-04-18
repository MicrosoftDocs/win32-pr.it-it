---
title: Abilitazione della sincronizzazione con Windows Media Player
description: Abilitazione della sincronizzazione con Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Gestione dispositivi, sincronizzazione con Windows Media Player
- Gestione dispositivi, sincronizzazione con Windows Media Player
- Guida per programmatori, sincronizzazione con Windows Media Player
- provider di servizi, sincronizzazione con Windows Media Player
- creazione di provider di servizi, sincronizzazione con Windows Media Player
- sincronizzazione con Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298987"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Abilitazione della sincronizzazione con Windows Media Player

È possibile consentire a un dispositivo di partecipare alla sincronizzazione automatica con Windows Media Player. Con la sincronizzazione automatica, quando un dispositivo sincronizzato definito dall'utente si connette al computer, Windows Media Player scaricherà, aggiornerà o eliminerà automaticamente i file dal dispositivo senza richiedere input utente aggiuntivi.

Per impostazione predefinita, i dispositivi seguenti sono sincronizzati con Windows Media Player:

-   Dispositivi MTP
-   Dispositivi di archiviazione di massa
-   Dispositivi Windows CE (Windows Media Player 10 mobile e versioni successive)

Per qualsiasi altro dispositivo da sincronizzare con Media Player di Windows, devono essere soddisfatti i requisiti seguenti:

-   Il dispositivo deve annunciare un'interfaccia del dispositivo PAP {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}
-   Gli oggetti dispositivo restituiti dal provider di servizi devono supportare l'interfaccia **IMDSPDevice3** .
-   Il parametro UseExtendedWmdm del dispositivo deve essere impostato su un valore **DWORD** pari a 1. Per ulteriori informazioni, vedere [parametri del dispositivo](device-parameters.md) .
-   Il provider di servizi deve implementare le interfacce seguenti:

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> <dt>

[**Parametri del dispositivo**](device-parameters.md)
</dt> </dl>

 

 




