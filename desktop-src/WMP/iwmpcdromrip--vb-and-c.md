---
title: Interfaccia IWMPCdromRip (VB e C) (WMP. h)
description: Fornisce le proprietà e i metodi per gestire la copia, o il ripping, di tracce da un CD audio. il ritaglio di un CD usando l'interfaccia IWMPCdromRip ha lo stesso effetto del ripping della musica usando l'interfaccia utente di Windows Media Player.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- Interfaccia IWMPCdromRip (VB e C) Windows Media Player
- Interfaccia IWMPCdromRip (VB e C) Windows Media Player, descritta
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
ms.openlocfilehash: 7d069fd8bd727d6a2a380c2ef29ce7c086db88d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328219"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>Interfaccia IWMPCdromRip (VB e C#)

Fornisce le proprietà e i metodi per gestire la copia, o l' *estrazione*, di tracce da un CD audio.

La copia di un CD usando l'interfaccia **IWMPCdromRip** ha lo stesso effetto del ritaglio di musica usando l'interfaccia utente di Windows Media Player. Il contenuto Ripped viene aggiunto automaticamente alla libreria in base alle preferenze dell'utente. Per ulteriori informazioni sulle preferenze utente per il ritaglio di CD, vedere la sezione relativa alla copia di musica da CDs nella Guida di Windows Media Player.

L'interfaccia **IWMPCdromRip** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPCdromRip (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPCdromRip (VB e C#)** presenta questi metodi.



| Metodo                                                                 | Descrizione                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | Estrae il CD.<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Arresta il processo di ripping del CD.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPCdromRip (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                | Tipo di accesso          | Descrizione                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripProgress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene lo stato di ripping del CD come percentuale di completamento.<br/>                                  |
| [**ripState**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene un valore di enumerazione che indica lo stato corrente del processo di estrazione.<br/> |



 

Ottenere un'interfaccia **IWMPCdromRip** eseguendo il cast dell'interfaccia **IWMPCdrom** del CD che si vuole copiare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Copia di un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





