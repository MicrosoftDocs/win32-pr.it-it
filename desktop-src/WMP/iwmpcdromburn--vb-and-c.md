---
title: Interfaccia IWMPCdrom(VB e C) (Wmp.h)
description: Fornisce proprietà e metodi per gestire la creazione di CD audio.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- Interfaccia IWMPCdromBurn (VB e C) Windows Media Player
- Interfaccia IWMPCdrom(VB e C) Windows Media Player , descritta
topic_type:
- apiref
api_name:
- IWMPCdromBurn (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731d5491e683c2a5d2e577c41dc96264c90f0d070538405d0fa3c3ea7283a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575959"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>Interfaccia IWMPCdromBurn (VB e C#)

Fornisce proprietà e metodi per gestire la creazione di CD audio.

## <a name="members"></a>Membri

**L'interfaccia IWMPCdromNz (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IWMPCdromBurn (VB e C#).**



| Metodo                                                                             | Descrizione                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Cancella il CD corrente.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Recupera il valore dell'attributo specificato per il CD.<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Fornisce informazioni sull'unità CD e sul supporto.<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Aggiorna le informazioni sullo stato per la playlist di masterizzazione corrente.<br/> |
| [**startBurn**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Masterizza il CD.<br/>                                                 |
| [**stopBurn**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Arresta il processo di masterizzazione cd.<br/>                                 |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IWMPCdromBurn (VB e C#)** ha queste proprietà.



| Proprietà                                                                                    | Tipo di accesso          | Descrizione                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnFormat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Sola lettura<br/> | Ottiene un valore che indica il tipo di CD da masterizzare.<br/>              |
| [**burnPlaylist**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene la playlist corrente da masterizzare nel CD.<br/>                     |
| [**burnProgress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene lo stato di avanzamento della masterizzazione cd come percentuale di completamento.<br/>                |
| [**burnState**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene un valore di enumerazione che indica lo stato di masterizzazione corrente.<br/> |
| [**Etichetta**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Sola lettura<br/> | Ottiene la stringa dell'etichetta del volume CD.<br/>                                 |



 

Ottenere **un'interfaccia IWMPCdromBurn** eseguendo il cast **dell'interfaccia IWMPCdrom** del CD da masterizzare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





