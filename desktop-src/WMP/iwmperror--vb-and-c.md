---
title: Interfaccia IWMPError (VB e C) (Wmp.h)
description: Fornisce proprietà e metodi per accedere a una raccolta di interfacce IWMPErrorItem per il recupero delle informazioni sugli errori. L'interfaccia IWMPError espone le proprietà seguenti.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- Interfaccia IWMPError (VB e C) Windows Media Player
- Interfaccia IWMPError (VB e C) Windows Media Player , descritta
topic_type:
- apiref
api_name:
- IWMPError (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3ff7635e423d70447e371d61fbbadf02aa14c2476e118be79cbb25d974348b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736181"
---
# <a name="iwmperror-vb-and-c-interface"></a>Interfaccia IWMPError (VB e C#)

Fornisce proprietà e metodi per accedere a una raccolta di **interfacce IWMPErrorItem** per il recupero delle informazioni sugli errori.

**L'interfaccia IWMPError** espone le proprietà seguenti.

## <a name="members"></a>Membri

**L'interfaccia IWMPError (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IWMPError (VB e C#).**



| Metodo                                                                         | Descrizione                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearErrorQueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | Cancella gli errori dalla coda degli errori.<br/>                                                                                            |
| [**Webhelp**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | Avvia la pagina microsoft Windows Media Player Guida Web per visualizzare altre informazioni sul primo errore nella coda degli errori.<br/> |



 

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IWMPError (VB e C#).**



| Proprietà                                                                        | Tipo di accesso           | Descrizione                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | Sola lettura<br/>  | Ottiene il numero di errori nella coda degli errori.<br/>                                                                            |
| [**Elemento**](iwmperror-item--vb-and-c.md)<br/>                             | Lettura/Scrittura<br/> | Ottiene **un'interfaccia IWMPErrorItem** in corrispondenza dell'indice specificato nella coda degli errori. In C# si tratta del **metodo get \_ Item.**<br/> |



 

Ottenere **un'interfaccia IWMPError** usando la proprietà seguente.



| Oggetto                                                                   | Proprietà                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Errore**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





