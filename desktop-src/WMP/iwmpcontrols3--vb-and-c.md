---
title: Interfaccia IWMPControls3 (VB e C) (WMP. h)
description: Fornisce proprietà e metodi per la selezione e il supporto della lingua audio che integrano l'interfaccia IWMPControls2. Oltre alle proprietà e ai metodi ereditati da IWMPControls2, l'interfaccia IWMPControls3 espone le proprietà seguenti.
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- Interfaccia IWMPControls3 (VB e C) Windows Media Player
- Interfaccia IWMPControls3 (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPControls3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9788dbd1b5910d655cbaa17055c76a0ae6d0280e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330731"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>Interfaccia IWMPControls3 (VB e C#)

Fornisce proprietà e metodi per la selezione e il supporto della lingua audio che integrano l'interfaccia **IWMPControls2** .

Oltre alle proprietà e ai metodi ereditati da **IWMPControls2**, l'interfaccia **IWMPControls3** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPControls3 (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPControls3 (VB e C#)** presenta questi metodi.



| Metodo                                                                                                         | Descrizione                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**getAudioLanguageDescription**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | Restituisce la descrizione della lingua audio corrispondente all'indice in base 1 specificato.<br/> |
| [**getAudioLanguageID**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | Restituisce l'LCID per un indice di lingua audio specificato.<br/>                                         |
| [**getLanguageName**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | Restituisce il nome della lingua audio con l'LCID specificato.<br/>                                |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPControls3 (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                                              | Tipo di accesso           | Descrizione                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**audioLanguageCount**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | Sola lettura<br/>  | Ottiene il numero di lingue audio supportate. <br/>                                                                                            |
| [**currentAudioLanguage**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione. <br/>                                                           |
| [**currentAudioLanguageIndex**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'indice in base uno che corrisponde alla lingua audio per la riproduzione. <br/>                                                   |
| [**currentPositionTimecode**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta la posizione corrente nell'elemento multimediale corrente utilizzando un formato di codice temporale. Questa proprietà attualmente supporta il codice ora SMPTE. <br/> |



 

Ottenere un'interfaccia **IWMPControls3** eseguendo il cast del valore restituito dalla proprietà [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls2 (VB e C#)**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





