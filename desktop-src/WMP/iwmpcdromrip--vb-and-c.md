---
title: Interfaccia IWMPCdromRip (VB e C) (Wmp.h)
description: Fornisce proprietà e metodi per gestire la copia o il ripping di tracce da un CD audio. Il ripping di un CD tramite l'interfaccia IWMPCdromRip ha lo stesso effetto di ripping della musica tramite l'interfaccia utente Windows Media Player.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- Interfaccia IWMPCdromRip (VB e C) Windows Media Player
- Interfaccia IWMPCdromRip (VB e C) Windows Media Player , descritta
topic_type:
- apiref
api_name:
- IWMPCdromRip (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a418f71ad8605e81115fa9ef1a45488a6830db94c260ef60aa0d991724d80a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747937"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>Interfaccia IWMPCdromRip (VB e C#)

Fornisce proprietà e metodi per gestire la copia o *lo scheggiamento* di tracce da un CD audio.

Il ripping di un CD tramite **l'interfaccia IWMPCdromRip** ha lo stesso effetto di ripping della musica usando l'Windows Media Player utente. Il contenuto decompresso viene aggiunto automaticamente alla libreria in base alle preferenze dell'utente. Per altre informazioni sulle preferenze utente per lo ripping di CD, vedere "Ripping di musica da CD" nella Guida di Windows Media Player.

**L'interfaccia IWMPCdromRip** espone le proprietà seguenti.

## <a name="members"></a>Membri

**L'interfaccia IWMPCdromRip (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IWMPCdromRip (VB e C#).**



| Metodo                                                                 | Descrizione                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | Copia il CD.<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Arresta il processo di ripping cd.<br/> |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili **nell'interfaccia IWMPCdromRip (VB e C#).**



| Proprietà                                                                                | Tipo di accesso          | Descrizione                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripProgress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene lo stato di avanzamento dello scheggiamento cd come percentuale di completamento.<br/>                                  |
| [**ripState**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene un valore di enumerazione che indica lo stato corrente del processo di depping.<br/> |



 

Ottenere **un'interfaccia IWMPCdromRip** eseguendo il cast **dell'interfaccia IWMPCdrom** del CD da copiare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Ripping di un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





