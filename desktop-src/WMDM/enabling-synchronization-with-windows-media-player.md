---
title: Abilitazione della sincronizzazione con Windows Media Player
description: Abilitazione della sincronizzazione con Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Gestione dispositivi multimediali, sincronizzazione con Windows Media Player
- Gestione dispositivi, sincronizzazione con Windows Media Player
- guida alla programmazione, sincronizzazione con Windows Media Player
- provider di servizi, sincronizzazione con Windows Media Player
- creazione di provider di servizi, sincronizzazione con Windows Media Player
- sincronizzazione con Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef06dd0e32e0ea95674f54b94336ecb6882e8215775c857ee0780a58b71af75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585009"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Abilitazione della sincronizzazione con Windows Media Player

È possibile abilitare un dispositivo per la sincronizzazione automatica con Windows Media Player. La sincronizzazione automatica significa che quando un dispositivo sincronizzato designato dall'utente si connette al computer, Windows Media Player scarica, aggiorna o elimina automaticamente i file dal dispositivo senza richiedere alcun input utente aggiuntivo.

Per impostazione predefinita, i dispositivi seguenti sono sincronizzati con Windows Media Player:

-   Dispositivi MTP
-   Dispositivi di archiviazione di massa
-   Windows CE dispositivi (Windows Media Player 10 Mobile e versioni successive)

Per sincronizzare qualsiasi altro dispositivo con Windows Media Player, devono essere soddisfatti i requisiti seguenti:

-   Il dispositivo deve annunciare un'interfaccia del dispositivo PAP {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}
-   Gli oggetti dispositivo restituiti dal provider di servizi devono supportare **l'interfaccia IMDSPDevice3.**
-   Il parametro del dispositivo UseExtendedWmdm deve essere impostato su un **valore DWORD** pari a 1. Per [altre informazioni, vedere Parametri](device-parameters.md) del dispositivo.
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

 

 




