---
description: Il metodo ProvideQualifiedComponent dell'oggetto Installer restituisce il percorso completo del componente ed esegue qualsiasi installazione necessaria. Se necessario, questo metodo richiede l'origine e incrementa il conteggio di utilizzo per la funzionalità.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Metodo Installer.ProvideQualifiedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 534f0d29fed41a495c3432ff757d7e269c6b2a5d63c9bfabebe614849f3ab9f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828871"
---
# <a name="installerprovidequalifiedcomponent-method"></a>Metodo Installer.ProvideQualifiedComponent

Il **metodo ProvideQualifiedComponent** dell'oggetto [**Installer**](installer-object.md) restituisce il percorso completo del componente ed esegue qualsiasi installazione necessaria. Se necessario, questo metodo richiede l'origine e incrementa il conteggio di utilizzo per la funzionalità.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Categoria* 
</dt> <dd>

Specifica l'ID componente per il componente richiesto. Potrebbe non trattarsi del GUID per il componente stesso, ma piuttosto di un server che fornisce la funzionalità corretta, come nella colonna ComponentId della [tabella PublishComponent](publishcomponent-table.md).

</dd> <dt>

*Qualifier* 
</dt> <dd>

Specifica un qualificatore in un elenco di componenti pubblicitari (dalla [tabella PublishComponent](publishcomponent-table.md)).

</dd> <dt>

*InstallMode* 
</dt> <dd>

Definisce la modalità di installazione. Questo parametro può essere uno dei valori illustrati nella tabella seguente.



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | Significato                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                 | Fornisce il componente , eseguendo qualsiasi installazione necessaria.<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>–1</dt> </dl>                                                                            | Fornisce il componente solo se la funzionalità esiste; in caso contrario, restituisce una stringa vuota. Questa modalità verifica l'esistenza del file di chiave del componente.<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt> </dl>                                                                | Fornisce il componente solo se la funzionalità esiste; in caso contrario, restituisce una stringa vuota. Questa modalità controlla solo che il componente sia registrato, ma non verifica l'esistenza del file di chiave del componente.<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                    | Fornisce il percorso del componente solo se la funzionalità esiste con un parametro InstallState *di msiInstallStateLocal.* In questo modo viene verificata la registrazione del componente, ma non viene verificata l'esistenza del file di chiave del componente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinazione dei flag msiReinstallMode**</dt> <dt></dt> </dl> | Chiama [**ReinstallFeature per**](installer-reinstallfeature.md) reinstallare la funzionalità usando questo parametro per il *parametro ReinstallMode* e quindi fornisce il componente.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




