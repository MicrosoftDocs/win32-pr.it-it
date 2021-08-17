---
description: Il metodo InstallProduct dell'oggetto Installer apre un pacchetto del programma di installazione e inizializza una sessione di installazione.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Metodo Installer.InstallProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1605fc0f2e955d6f0364159779ae90f8f59e9ace0f3ff14a1106f7623ab7d99d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630393"
---
# <a name="installerinstallproduct-method"></a>Metodo Installer.InstallProduct

Il **metodo InstallProduct** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto del programma di installazione e inizializza una sessione di installazione.

## <a name="syntax"></a>Sintassi


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*packagePath* 
</dt> <dd>

Stringa obbligatoria contenente il percorso del pacchetto di installazione.

</dd> <dt>

*propertyValues* 
</dt> <dd>

Stringa facoltativa contenente coppie property=value separate da spazi vuoti.

Per eseguire un'installazione amministrativa, includere ACTION=ADMIN in *propertyValues*. Per altre informazioni, vedere la [**proprietà ACTION.**](action.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per rimuovere completamente un prodotto, impostare REMOVE=ALL in *propertyValues*. Per altre informazioni, vedere [**La proprietà REMOVE.**](remove.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




