---
title: Interfaccia IWMPSettings2 (VB e C) (WMP. h)
description: Fornisce le proprietà e un metodo che integrano l'interfaccia IWMPSettings. Oltre alle proprietà e ai metodi ereditati da IWMPSettings, l'interfaccia IWMPSettings2 espone le proprietà seguenti.
ms.assetid: 6bd0f6dd-df49-4c21-b47c-c8c63f85c2c0
keywords:
- Interfaccia IWMPSettings2 (VB e C) Windows Media Player
- Interfaccia IWMPSettings2 (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPSettings2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb782433085544a94db0eab6b9314f1e4df488e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332557"
---
# <a name="iwmpsettings2-vb-and-c-interface"></a>Interfaccia IWMPSettings2 (VB e C#)

Fornisce le proprietà e un metodo che integrano l'interfaccia **IWMPSettings** .

Oltre alle proprietà e ai metodi ereditati da **IWMPSettings**, l'interfaccia **IWMPSettings2** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPSettings2 (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPSettings2 (VB e C#)** presenta questi metodi.



| Metodo                                                                                                   | Descrizione                                                     |
|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**requestMediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md) | Richiede un livello specificato di accesso alla libreria.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPSettings2 (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                                    | Tipo di accesso          | Descrizione                                                                               |
|:------------------------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**defaultAudioLanguage**](wmplibiwmpsettings2-iwmpsettings2-defaultaudiolanguage--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita. <br/>              |
| [**mediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene un valore che indica le autorizzazioni attualmente concesse per l'accesso alla libreria. <br/> |



 

Ottenere un'interfaccia **IWMPSettings2** eseguendo il cast del valore restituito dalla proprietà **AxWindowsMediaPlayer. Settings** .



| Oggetto                                                                   | Proprietà                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Impostazioni**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





