---
description: La proprietà QualifierDescription di sola lettura restituisce una stringa di testo che descrive il componente completo.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Proprietà Installer.QualifierDescription
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
ms.openlocfilehash: c226f00d7f95b4585fa4a0713fb281011079cdc35c4e421254beec75db84d7db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763581"
---
# <a name="installerqualifierdescription-property"></a>Proprietà Installer.QualifierDescription

La proprietà **QualifierDescription** di sola lettura restituisce una stringa di testo che descrive il componente completo. Questa stringa localizzabile viene creato nella colonna AppData della tabella [PublishComponent](publishcomponent-table.md) e può essere visualizzata all'utente. Il qualificatore distingue più forme dello stesso componente, ad esempio un componente implementato in più linguaggi.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Componenti qualificati](qualified-components.md)
</dt> </dl>

 

 




