---
description: Il metodo RemovePatches rimuove una o più patch ai prodotti idonei per la ricezione della patch. Il metodo RemovePatches chiama MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Installer. RemovePatches, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329124"
---
# <a name="installerremovepatches-method"></a>Installer. RemovePatches, metodo

Il metodo **RemovePatches** rimuove una o più patch ai prodotti idonei per la ricezione della patch. Il metodo **RemovePatches** chiama [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).

## <a name="syntax"></a>Sintassi


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Applicazione di patch* 
</dt> <dd>

Stringa che contiene un elenco delimitato da punti e virgola di patch da rimuovere. Ogni patch può essere rappresentata dal percorso completo del pacchetto di patch o dal GUID della patch. Questo parametro è obbligatorio.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Stringa con il GUID del prodotto da cui devono essere rimosse le patch. Questo parametro è obbligatorio.

</dd> <dt>

*UninstallType* 
</dt> <dd>

Valore intero che specifica il tipo di rimozione della patch. Questo parametro deve essere **msiInstallTypeSingleInstance**.

</dd> <dt>

*PropertyList* 
</dt> <dd>

Stringa che specifica le coppie proprietà = valore da includere. Questo parametro è facoltativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Vedere [disinstallazione di patch](uninstalling-patches.md) per un esempio che illustra come un'applicazione può rimuovere una patch da tutti i prodotti disponibili per l'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Disinstallazione di patch](uninstalling-patches.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




