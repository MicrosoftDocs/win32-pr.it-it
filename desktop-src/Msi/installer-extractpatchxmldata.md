---
description: Il metodo ExtractPatchXMLData dell'oggetto Installer estrae le informazioni da una patch come stringa XML. Le informazioni possono essere usate per determinare se la patch si applica a un sistema di destinazione. Questo metodo chiama MsiExtractPatchXMLData.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Metodo Installer.ExtractPatchXMLData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d9b4df7d2ecedda5e3bac97a1dd80a002571f736ceb2ede6b8deac2f1a5f7802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631544"
---
# <a name="installerextractpatchxmldata-method"></a>Metodo Installer.ExtractPatchXMLData

Il **metodo ExtractPatchXMLData** dell'oggetto [**Installer**](installer-object.md) estrae le informazioni da una patch come stringa XML. Le informazioni possono essere usate per determinare se la patch si applica a un sistema di destinazione. Questo metodo chiama [**MsiExtractPatchXMLData.**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)

## <a name="syntax"></a>Sintassi


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PatchPath* 
</dt> <dd>

Percorso completo della patch da cui estrarre le informazioni sull'applicabilità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva Windows Server 2003 o Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




