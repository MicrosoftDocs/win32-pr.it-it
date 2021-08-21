---
description: Il metodo ConfigureProduct dell'oggetto Installer installa o disinstalla un prodotto.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configmetodo ureProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7fd64424105bc06364abf2b047ba4d986fdd5540d007109dfb9fdc087250c194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632158"
---
# <a name="installerconfigureproduct-method"></a>Installer.Configmetodo ureProduct

Il **metodo ConfigureProduct** dell'oggetto [**Installer**](installer-object.md) installa o disinstalla un prodotto.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Prodotto* 
</dt> <dd>

Specifica il codice prodotto del prodotto.

</dd> <dt>

*InstallLevel* 
</dt> <dd>

Specifica la configurazione di installazione predefinita del prodotto. Il parametro InstallLevel viene ignorato e tutte le funzionalità vengono installate se il parametro InstallState è impostato su un valore diverso da msiInstallStateDefault.

Questo parametro deve essere 0 (installazione con livelli di funzionalità creati), 65535 (installare tutte le funzionalità) o un valore compreso tra 0 e 65535 per installare un subset di funzionalità disponibili.

</dd> <dt>

*InstallState* 
</dt> <dd>

Specifica lo stato di installazione per la funzionalità. Questo parametro deve essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                        | Significato                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiInstallStateAdvertised**</dt> </dl> | La funzionalità viene annunciata<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiInstallStateLocal**</dt> </dl>                     | La funzionalità viene installata in locale.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiInstallStateAbsent**</dt> </dl>                 | La funzionalità viene disinstallata.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiInstallStateSource**</dt> </dl>                 | La funzionalità viene installata per l'esecuzione dall'origine.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiInstallStateDefault**</dt> </dl>             | La funzionalità viene installata nel percorso predefinito.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo ConfigureProduct** visualizza l'interfaccia utente usando le impostazioni correnti. Le impostazioni dell'interfaccia utente possono essere modificate modificando la [**proprietà UILevel (oggetto Installer)**](installer-uilevel.md) prima di chiamare il **metodo ConfigureProduct.**

Se il *parametro InstallState* è impostato su un valore diverso da msiInstallStateDefault, il *parametro InstallLevel* viene ignorato e vengono installate tutte le funzionalità del prodotto. Usare il [**metodo ConfigureFeature**](installer-configurefeature.md) per controllare l'installazione di singole funzionalità quando il *parametro InstallState* non è impostato su msiInstallStateDefault.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[Funzioni di installazione e configurazione](installer-function-reference.md)
</dt> </dl>

 

 




