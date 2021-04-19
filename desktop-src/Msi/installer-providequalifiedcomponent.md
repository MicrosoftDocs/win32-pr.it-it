---
description: Il metodo ProvideQualifiedComponent dell'oggetto Installer restituisce il percorso completo del componente ed esegue tutte le installazioni necessarie. Se necessario, questo metodo richiede l'origine e incrementa il conteggio di utilizzo per la funzionalità.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Installer. ProvideQualifiedComponent, metodo
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
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329127"
---
# <a name="installerprovidequalifiedcomponent-method"></a>Installer. ProvideQualifiedComponent, metodo

Il metodo **ProvideQualifiedComponent** dell'oggetto [**Installer**](installer-object.md) restituisce il percorso completo del componente ed esegue tutte le installazioni necessarie. Se necessario, questo metodo richiede l'origine e incrementa il conteggio di utilizzo per la funzionalità.

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

Specifica l'ID componente per il componente richiesto. Potrebbe non essere il GUID per il componente stesso, bensì un server che fornisce la funzionalità corretta, come nella colonna ComponentId della [tabella PublishComponent](publishcomponent-table.md).

</dd> <dt>

*Qualifier* 
</dt> <dd>

Specifica un qualificatore in un elenco di componenti pubblicitari (dalla [tabella PublishComponent](publishcomponent-table.md)).

</dd> <dt>

*InstallMode* 
</dt> <dd>

Definisce la modalità di installazione. Questo parametro può essere uno dei valori mostrati nella tabella seguente.



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | Significato                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                 | Fornisce il componente, eseguendo le installazioni necessarie.<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>-1</dt> </dl>                                                                            | Fornisce il componente solo se la funzionalità esiste; in caso contrario, restituisce una stringa vuota. Questa modalità verifica l'esistenza del file di chiave del componente.<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt> </dl>                                                                | Fornisce il componente solo se la funzionalità esiste; in caso contrario, restituisce una stringa vuota. Questa modalità controlla solo che il componente sia registrato, ma non verifica l'esistenza del file di chiave del componente.<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                    | Fornisce il percorso del componente solo se la funzionalità esiste con un parametro InstallState di *msiInstallStateLocal*. Questa operazione Controlla la registrazione del componente, ma non verifica l'esistenza del file di chiave del componente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinazione dei flag msiReinstallMode**</dt> <dt></dt> </dl> | Chiama [**ReinstallFeature**](installer-reinstallfeature.md) per reinstallare la funzionalità utilizzando questo parametro per il parametro *REINSTALLMODE* e quindi fornisce il componente.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




