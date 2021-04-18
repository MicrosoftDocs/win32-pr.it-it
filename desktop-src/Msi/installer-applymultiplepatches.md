---
description: Il metodo ApplyMultiplePatches applica una o più patch ai prodotti idonei per la ricezione della patch. Il metodo imposta la proprietà PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Installer. ApplyMultiplePatches, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328321"
---
# <a name="installerapplymultiplepatches-method"></a>Installer. ApplyMultiplePatches, metodo

Il metodo **ApplyMultiplePatches** applica una o più patch ai prodotti idonei per la ricezione della patch. Il metodo imposta la proprietà [**patch**](patch.md) .

## <a name="syntax"></a>Sintassi


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PatchPackagesList* 
</dt> <dd>

Stringa che contiene un elenco delimitato da punti e virgola dei percorsi dei file di patch. Ad esempio: "" c: \\ SUS \\ download \\ cache \\ Office \\ SP1. msp; c: \\ cache di download di SUS \\ \\ \\ Office \\ QFE1. msp; c: \\ SUS \\ download \\ cache \\ Office \\ QFEn. msp ""

</dd> <dt>

*Prodotto* 
</dt> <dd>

Questo parametro fornisce il [**ProductCode**](productcode.md) del prodotto a cui viene applicata la patch. Questo parametro è facoltativo. Quando questo parametro è null, le patch vengono applicate a tutti i prodotti idonei per la ricezione di tali patch.

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

Stringa con terminazione null che specifica le impostazioni della proprietà della riga di comando. Questo parametro è facoltativo. Vedere [informazioni sulle proprietà](about-properties.md) e [impostazione dei valori delle proprietà pubbliche nella riga di comando](setting-public-property-values-on-the-command-line.md). Queste proprietà sono condivise da tutti i prodotti di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**PATCH**](patch.md)
</dt> <dt>

[Impostazione dei valori delle proprietà pubbliche nella riga di comando](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




