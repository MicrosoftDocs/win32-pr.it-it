---
description: L'oggetto FeatureInfo contiene informazioni relative alla funzionalità di destinazione e viene creato dall'oggetto Session usando il metodo FeatureInfo.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Oggetto FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324241"
---
# <a name="featureinfo-object"></a>Oggetto FeatureInfo

L'oggetto **FeatureInfo** contiene informazioni relative alla funzionalità di destinazione e viene creato dall'oggetto [**Session**](session-object.md) usando il metodo [**FeatureInfo**](session-featureinfo.md) .

## <a name="members"></a>Membri

L'oggetto **FeatureInfo** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **FeatureInfo** dispone di queste proprietà.



| Proprietà                                                  | Tipo di accesso           | Descrizione                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Attributi**](featureinfo-attributes.md)<br/>   | Lettura/Scrittura<br/> | Restituisce il valore per la funzionalità nella colonna Attributes della tabella Feature.<br/> |
| [**Descrizione**](featureinfo-description.md)<br/> |                       | Restituisce la descrizione della funzionalità.<br/>                                          |
| [**Titolo**](featureinfo-title.md)<br/>             | Sola lettura<br/>  | Restituisce il titolo della funzionalità.<br/>                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo è definito come 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




