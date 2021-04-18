---
title: Interfaccia IWMPCdromCollection (VB e C) (WMP. h)
description: Fornisce un modo per organizzare e accedere a una raccolta di unità CD o DVD. L'interfaccia IWMPCdromCollection espone la proprietà seguente.
ms.assetid: 60874603-d9c8-4ed1-a92a-bd069bd0c253
keywords:
- Interfaccia IWMPCdromCollection (VB e C) Windows Media Player
- Interfaccia IWMPCdromCollection (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPCdromCollection (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fbc9c053c186b6d542e201f7bee5d2331b649
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330734"
---
# <a name="iwmpcdromcollection-vb-and-c-interface"></a>Interfaccia IWMPCdromCollection (VB e C#)

Fornisce un modo per organizzare e accedere a una raccolta di unità CD o DVD.

L'interfaccia **IWMPCdromCollection** espone la proprietà seguente.

## <a name="members"></a>Membri

L'interfaccia **IWMPCdromCollection (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPCdromCollection (VB e C#)** presenta questi metodi.



| Metodo                                                                                                     | Descrizione                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**getByDriveSpecifier**](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md) | Restituisce un'interfaccia **IWMPCdrom** associata a una lettera di unità specifica.<br/> |
| [**Elemento**](wmplibiwmpcdromcollection-iwmpcdromcollection-item--vb-and-c.md)                               | Restituisce un'interfaccia **IWMPCdrom** in corrispondenza dell'indice specificato.<br/>                        |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPCdromCollection (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                  | Tipo di accesso          | Descrizione                                                              |
|:------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------|
| [**count**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene il numero di unità CD e DVD disponibili nel sistema.<br/> |



 

Ottenere un'interfaccia **IWMPCdromCollection** usando la proprietà seguente.



| Oggetto                                                                   | Proprietà                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**cdromcollection**](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> </dl>

 

 





