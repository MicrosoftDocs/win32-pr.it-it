---
description: La proprietà QualifierDescription di sola lettura restituisce una stringa di testo che descrive il componente completo.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Proprietà Installer. QualifierDescription
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332170"
---
# <a name="installerqualifierdescription-property"></a>Proprietà Installer. QualifierDescription

La proprietà **QualifierDescription** di sola lettura restituisce una stringa di testo che descrive il componente completo. Questa stringa localizzabile viene creata nella colonna AppData della [tabella PublishComponent](publishcomponent-table.md) e può essere visualizzata all'utente. Il qualificatore distingue più forme dello stesso componente, ad esempio un componente implementato in più lingue.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Componenti qualificati](qualified-components.md)
</dt> </dl>

 

 




