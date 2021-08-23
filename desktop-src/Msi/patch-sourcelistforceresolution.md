---
description: Il metodo SourceListForceResolution cancella l'ultima proprietà source usata.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Metodo Patch.SourceListForceResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a02e538a1d61fb0adf081542f10dea29f2a636e36b9ce936d7d282e30823339d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065861"
---
# <a name="patchsourcelistforceresolution-method"></a>Metodo Patch.SourceListForceResolution

Il **metodo SourceListForceResolution** cancella l'ultima proprietà source usata. In questo modo il programma di installazione cerca nell'elenco di origine un'origine patch valida alla successiva richiesta dell'origine della patch. Ad esempio, il programma di installazione richiede l'origine della patch per eseguire un'installazione o una reinstallazione quando manca la copia della cache locale della patch. Questo metodo chiama [**MsiSourceListForceResolution.**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)

## <a name="syntax"></a>Sintassi


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IPatch IID è definito come \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




