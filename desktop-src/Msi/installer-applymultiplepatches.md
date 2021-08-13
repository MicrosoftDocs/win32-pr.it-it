---
description: Il metodo ApplyMultiplePatches applica una o più patch ai prodotti idonei per la ricezione della patch. Il metodo imposta la proprietà PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Metodo Installer.ApplyMultiplePatches
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
ms.openlocfilehash: a2b1c469ca623b0c09ea2899de1867cc10c8d8cda9363994973d08ecc20ed7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633208"
---
# <a name="installerapplymultiplepatches-method"></a>Metodo Installer.ApplyMultiplePatches

Il **metodo ApplyMultiplePatches** applica una o più patch ai prodotti idonei per la ricezione della patch. Il metodo imposta la [**proprietà PATCH.**](patch.md)

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

Stringa che contiene un elenco delimitato da punto e virgola dei percorsi per applicare patch ai file. Ad esempio: ""c: \\ sus \\ download cache Office \\ \\ \\ sp1.msp; c: \\ sus \\ download cache \\ Office \\ \\ QFE1.msp;c: \\ sus download cache Office \\ \\ \\ \\ QFEn.msp""

</dd> <dt>

*Prodotto* 
</dt> <dd>

Questo parametro fornisce il [**Codice Prodotto del**](productcode.md) prodotto a cui applicare la patch. Questo parametro è facoltativo. Quando questo parametro è Null, le patch vengono applicate a tutti i prodotti idonei per la ricezione di tali patch.

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

Stringa con terminazione Null che specifica le impostazioni delle proprietà della riga di comando. Questo parametro è facoltativo. Vedere [Informazioni sulle proprietà](about-properties.md) e Impostazione dei valori delle proprietà pubbliche nella riga di [comando.](setting-public-property-values-on-the-command-line.md) Queste proprietà sono condivise da tutti i prodotti di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003 o Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**benda**](patch.md)
</dt> <dt>

[Impostazione dei valori delle proprietà pubbliche nella riga di comando](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




