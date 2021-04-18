---
title: Interfaccia IWMPLibrary (VB e C) (WMP. h)
description: Rappresenta una libreria. L'interfaccia IWMPLibrary espone le proprietà seguenti.
ms.assetid: 956b2da1-5f01-48d6-8faa-e360c225afda
keywords:
- Interfaccia IWMPLibrary (VB e C) Windows Media Player
- Interfaccia IWMPLibrary (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPLibrary (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9749d3a2363c3863180639f249d7261ec1b9694
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330723"
---
# <a name="iwmplibrary-vb-and-c-interface"></a>Interfaccia IWMPLibrary (VB e C#)

Rappresenta una libreria.

L'interfaccia **IWMPLibrary** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPLibrary (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPLibrary (VB e C#)** presenta questi metodi.



| Metodo                                                                     | Descrizione                                                                                           |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Identico**](wmplibiwmplibrary-iwmplibrary-isidentical--vb-and-c.md) | Restituisce un valore che indica se l'oggetto fornito è uguale a quello corrente.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPLibrary (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                      | Tipo di accesso          | Descrizione                                                                   |
|:----------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene un'interfaccia **IWMPMediaCollection** per la libreria corrente.<br/> |
| [**nome**](wmplibiwmplibrary-iwmplibrary-name--vb-and-c.md)<br/>                       | Sola lettura<br/> | Ottiene il nome visualizzato della libreria corrente.<br/>                      |
| [**tipo**](wmplibiwmplibrary-iwmplibrary-type--vb-and-c.md)<br/>                       | Sola lettura<br/> | Ottiene un valore che indica il tipo di libreria.<br/>                      |



 

Ottenere un'interfaccia **IWMPLibrary** usando il metodo seguente.



| Oggetto                                                   | Proprietà                                                         |
|----------------------------------------------------------|------------------------------------------------------------------|
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md) | [**getLibraryByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPLibraryServices. getLibraryByType (VB e C#)**](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md)
</dt> </dl>

 

 





