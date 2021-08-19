---
description: Il metodo RemovePatches rimuove una o più patch ai prodotti idonei per la ricezione della patch. Il metodo RemovePatches chiama MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Metodo Installer.RemovePatches
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
ms.openlocfilehash: bfa316b4ff01f6e5667b3fb2c5fce2333c4b4aaf34dc5a1dbb37feb61d1a9ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894031"
---
# <a name="installerremovepatches-method"></a>Metodo Installer.RemovePatches

Il **metodo RemovePatches** rimuove una o più patch ai prodotti idonei per la ricezione della patch. Il **metodo RemovePatches** chiama [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).

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

*PatchList* 
</dt> <dd>

Stringa che contiene un elenco delimitato da punto e virgola di patch da rimuovere. Ogni patch può essere rappresentata dal percorso completo del pacchetto di patch o dal GUID della patch. Questo parametro è obbligatorio.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Stringa con il GUID del prodotto da cui rimuovere le patch. Questo parametro è obbligatorio.

</dd> <dt>

*UninstallType* 
</dt> <dd>

Valore intero che specifica il tipo di rimozione della patch. Questo parametro deve essere **msiInstallTypeSingleInstance.**

</dd> <dt>

*Elenco delle proprietà* 
</dt> <dd>

Stringa che specifica le coppie Property=Value da includere. Questo parametro è facoltativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Vedere [Disinstallazione di patch per](uninstalling-patches.md) un esempio che illustra come un'applicazione può rimuovere una patch da tutti i prodotti disponibili per l'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003 o Windows XP.<br/> |
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

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




