---
description: Il metodo ConfigureFeature dell'oggetto Installer configura lo stato installato di una funzionalità del prodotto.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configmetodo ureFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 522dfffcbafd546dce218956729f01133708833a4a4c2732af3ea0248f87bc71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632347"
---
# <a name="installerconfigurefeature-method"></a>Installer.Configmetodo ureFeature

Il **metodo ConfigureFeature** dell'oggetto [**Installer**](installer-object.md) configura lo stato installato di una funzionalità del prodotto.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Prodotto* 
</dt> <dd>

Specifica il codice prodotto del prodotto.

</dd> <dt>

*Funzionalità* 
</dt> <dd>

Specifica l'ID funzionalità della funzionalità da configurare.

</dd> <dt>

*Stato di installazione* 
</dt> <dd>

Specifica lo stato di installazione per la funzionalità. Questo parametro deve essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                        | Significato                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiInstallStateAdvertised**</dt> </dl> | La funzionalità è annunciata<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiInstallStateLocal**</dt> </dl>                     | La funzionalità viene installata in locale.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiInstallStateAbsent**</dt> </dl>                 | La funzionalità viene disinstallata.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiInstallStateSource**</dt> </dl>                 | La funzionalità viene installata per l'esecuzione dall'origine.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiInstallStateDefault**</dt> </dl>             | La funzionalità viene installata nel percorso predefinito.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[Funzioni di installazione e configurazione](installer-function-reference.md)
</dt> </dl>

 

 




