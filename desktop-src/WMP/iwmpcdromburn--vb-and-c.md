---
title: Interfaccia IWMPCdromBurn (VB e C) (WMP. h)
description: Fornisce proprietà e metodi per la gestione della creazione di CD audio.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- Interfaccia IWMPCdromBurn (VB e C) Windows Media Player
- Interfaccia IWMPCdromBurn (VB e C) Windows Media Player, descritta
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
ms.openlocfilehash: d2fe21a20194f57e4a8b52a3ba05032a07cb31f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330735"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>Interfaccia IWMPCdromBurn (VB e C#)

Fornisce proprietà e metodi per la gestione della creazione di CD audio.

## <a name="members"></a>Membri

L'interfaccia **IWMPCdromBurn (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPCdromBurn (VB e C#)** presenta questi metodi.



| Metodo                                                                             | Descrizione                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Cancella il CD corrente.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Recupera il valore dell'attributo specificato per il CD.<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Fornisce informazioni sull'unità CD e sui supporti.<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Aggiorna le informazioni sullo stato per la playlist Burn corrente.<br/> |
| [**startBurn**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Masterizza il CD.<br/>                                                 |
| [**stopBurn**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Arresta il processo di masterizzazione del CD.<br/>                                 |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPCdromBurn (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                    | Tipo di accesso          | Descrizione                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnFormat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Sola lettura<br/> | Ottiene un valore che indica il tipo di CD da masterizzare.<br/>              |
| [**burnPlaylist**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene la playlist corrente da masterizzare nel CD.<br/>                     |
| [**burnProgress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene lo stato di avanzamento del CD come percentuale di completamento.<br/>                |
| [**burnState**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene un valore di enumerazione che indica lo stato Burn corrente.<br/> |
| [**etichetta**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Sola lettura<br/> | Ottiene la stringa dell'etichetta del volume CD.<br/>                                 |



 

Ottenere un'interfaccia **IWMPCdromBurn** eseguendo il cast dell'interfaccia **IWMPCdrom** del CD che si vuole masterizzare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





