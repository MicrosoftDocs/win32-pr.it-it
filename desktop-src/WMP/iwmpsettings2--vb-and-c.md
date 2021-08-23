---
title: Interfaccia IWMPSettings2 (VB e C ) (Wmp.h)
description: Fornisce proprietà e un metodo che integrano l'interfaccia IWMPSettings. Oltre alle proprietà e ai metodi ereditati da IWMPSettings, l'interfaccia IWMPSettings2 espone le proprietà seguenti.
ms.assetid: 6bd0f6dd-df49-4c21-b47c-c8c63f85c2c0
keywords:
- Interfaccia IWMPSettings2 (VB e C) Windows Media Player
- Interfaccia IWMPSettings2 (VB e C) Windows Media Player , descritta
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
ms.openlocfilehash: 4e227cc255eee625df926031369ef8be0fe270e377b143adff2c3ed2d9ab0aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135354"
---
# <a name="iwmpsettings2-vb-and-c-interface"></a>Interfaccia IWMPSettings2 (VB e C#)

Fornisce proprietà e un metodo che integrano **l'interfaccia IWMPSettings.**

Oltre alle proprietà e ai metodi ereditati da **IWMPSettings,** **l'interfaccia IWMPSettings2** espone le proprietà seguenti.

## <a name="members"></a>Membri

**L'interfaccia IWMPSettings2 (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IWMPSettings2 (VB e C#)** ha questi metodi.



| Metodo                                                                                                   | Descrizione                                                     |
|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**requestMediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md) | Richiede un livello di accesso specificato alla libreria.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IWMPSettings2 (VB e C#)** ha queste proprietà.



| Proprietà                                                                                                    | Tipo di accesso          | Descrizione                                                                               |
|:------------------------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**defaultAudioLanguage**](wmplibiwmpsettings2-iwmpsettings2-defaultaudiolanguage--vb-and-c.md)<br/> | Sola lettura<br/> | Ottiene l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita. <br/>              |
| [**mediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)<br/>       | Sola lettura<br/> | Ottiene un valore che indica le autorizzazioni attualmente concesse per l'accesso alla libreria. <br/> |



 

Ottenere **un'interfaccia IWMPSettings2** eseguendo il cast del valore restituito dalla **proprietà AxWindowsMediaPlayer.settings.**



| Oggetto                                                                   | Proprietà                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Impostazioni**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





