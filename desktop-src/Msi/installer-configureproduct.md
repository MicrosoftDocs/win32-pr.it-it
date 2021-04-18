---
description: Il metodo ConfigureProduct dell'oggetto Installer installa o Disinstalla un prodotto.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Metodo ureProduct Installer.Config
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
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333883"
---
# <a name="installerconfigureproduct-method"></a>Metodo ureProduct Installer.Config

Il metodo **ConfigureProduct** dell'oggetto [**Installer**](installer-object.md) installa o Disinstalla un prodotto.

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

Specifica il codice del prodotto.

</dd> <dt>

*InstallLevel* 
</dt> <dd>

Specifica la configurazione di installazione predefinita del prodotto. Il parametro InstallLevel viene ignorato e tutte le funzionalità vengono installate se il parametro InstallState è impostato su un valore diverso da msiInstallStateDefault.

Questo parametro deve essere 0 (installare usando i livelli di funzionalità creati), 65535 (installare tutte le funzionalità) oppure un valore compreso tra 0 e 65535 per installare un subset di funzionalità disponibili.

</dd> <dt>

*InstallState* 
</dt> <dd>

Specifica lo stato di installazione per la funzionalità. Questo parametro deve essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                        | Significato                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiInstallStateAdvertised**</dt> </dl> | La funzionalità è annunciata<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiInstallStateLocal**</dt> </dl>                     | La funzionalità viene installata localmente.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiInstallStateAbsent**</dt> </dl>                 | La funzionalità viene disinstallata.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiInstallStateSource**</dt> </dl>                 | La funzionalità è installata per l'esecuzione dall'origine.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiInstallStateDefault**</dt> </dl>             | La funzionalità viene installata nel percorso predefinito.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **ConfigureProduct** Visualizza l'interfaccia utente usando le impostazioni correnti. Le impostazioni dell'interfaccia utente possono essere modificate modificando la [**Proprietà UILevel (oggetto Installer)**](installer-uilevel.md) prima di chiamare il metodo **ConfigureProduct** .

Se il parametro *InstallState* è impostato su un valore diverso da msiInstallStateDefault, il parametro *InstallLevel* viene ignorato e tutte le funzionalità del prodotto sono installate. Usare il metodo [**ConfigureFeature**](installer-configurefeature.md) per controllare l'installazione di singole funzionalità quando il parametro *InstallState* non è impostato su msiInstallStateDefault.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[Funzioni di installazione e configurazione](installer-function-reference.md)
</dt> </dl>

 

 




