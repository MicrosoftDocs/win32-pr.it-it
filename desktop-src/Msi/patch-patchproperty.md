---
description: La proprietà PatchProperty ottiene informazioni su una patch specifica applicata a un'istanza specifica del prodotto. Questa proprietà chiama MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Patch. PatchProperty, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329469"
---
# <a name="patchpatchproperty-method"></a>Patch. PatchProperty, metodo

La proprietà **PatchProperty** ottiene informazioni su una patch specifica applicata a un'istanza specifica del prodotto. Questa proprietà chiama [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).

## <a name="syntax"></a>Sintassi


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szProperty* 
</dt> <dd>

Il parametro *szProperty* può essere uno dei valori seguenti.



| Nome          | Significato                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocalPackage  | Ottiene il file di patch memorizzato nella cache utilizzato dal prodotto.                                                                                                                                                                                                                                                                               |
| Trasformazioni    | Ottenere il set di trasformazioni di patch applicato al prodotto dall'ultima installazione della patch. Questo valore potrebbe non essere disponibile per le applicazioni non gestite per utente se l'utente non è connesso al computer.                                                                                                                     |
| InstallDate   | Ottenere la data in cui è stata applicata la patch al prodotto.                                                                                                                                                                                                                                                                      |
| Disinstallabili | Restituisce "1" se la patch è contrassegnata come possibile per la disinstallazione dal prodotto. In questo caso, il programma di installazione può comunque bloccare la disinstallazione se questa patch è richiesta da un'altra patch che non può essere disinstallata.                                                                                                          |
| State         | Restituisce "1" Se questa patch è attualmente applicata al prodotto. Restituisce "2" Se questa patch è stata sostituita da un'altra patch. Restituisce "4" Se questa patch è stata resa obsoleta da un'altra patch. Questi valori corrispondono alle costanti usate dal parametro *dwFilter* di [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa). |
| DisplayName   | Ottenere il nome visualizzato registrato per la patch. Per le patch che non includono la proprietà DisplayName nella tabella [MsiPatchMetadata](msipatchmetadata-table.md) , il nome visualizzato restituito è una stringa vuota ("").                                                                                                      |
| MoreInfoURL   | Ottenere l'URL delle informazioni di supporto registrato per la patch. Per le patch che non includono la proprietà MoreInfoURL nella tabella [MsiPatchMetadata](msipatchmetadata-table.md) , l'URL delle informazioni di supporto restituito è una stringa vuota ("").                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo può restituire \_ l'errore Unknown \_ patch, se l'oggetto [**patch**](patch-object.md) viene inizializzato con una stringa vuota per *ProductCode*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




