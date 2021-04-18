---
description: Il metodo InstallProduct dell'oggetto Installer apre un pacchetto di installazione e Inizializza una sessione di installazione.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Installer. InstallProduct, metodo
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
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324618"
---
# <a name="installerinstallproduct-method"></a>Installer. InstallProduct, metodo

Il metodo **InstallProduct** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto di installazione e Inizializza una sessione di installazione.

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

Stringa facoltativa che contiene le coppie proprietà = valore separate da spazi vuoti.

Per eseguire un'installazione amministrativa, includere ACTION = ADMIN in *propertyValues*. Per ulteriori informazioni, vedere la proprietà [**Action**](action.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per rimuovere completamente un prodotto, impostare REMOVE = ALL in *propertyValues*. Per ulteriori informazioni, vedere [**Remove**](remove.md) Property.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




