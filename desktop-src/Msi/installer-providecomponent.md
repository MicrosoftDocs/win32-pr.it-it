---
description: Il metodo ProvideComponent dell'oggetto Installer restituisce il percorso completo del componente ed esegue l'installazione necessaria.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Metodo Installer.ProvideComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 49e3808fdad44e4bc3cb7312c1b352874eab3b768920f23ac198811d29f6c8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630329"
---
# <a name="installerprovidecomponent-method"></a>Metodo Installer.ProvideComponent

Il **metodo ProvideComponent** dell'oggetto [**Installer**](installer-object.md) restituisce il percorso completo del componente ed esegue l'installazione necessaria. Se necessario, il **metodo ProvideComponent** dell'oggetto [**Installer**](installer-object.md) richiede l'origine e incrementa il numero di utilizzi per la funzionalità.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
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

Specifica l'ID funzionalità della funzionalità contenente il componente.

</dd> <dt>

*Componente* 
</dt> <dd>

Specifica il codice del componente.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Definisce la modalità di installazione. Questo parametro può essere uno dei valori illustrati nella tabella seguente.



| Nome                                                                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                | Fornisce il percorso del componente, eseguendo qualsiasi installazione, se necessario.<br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>–1</dt> </dl>                                                                           | Fornisce il percorso del componente solo se la funzionalità esiste; In caso contrario, restituisce una stringa vuota. Questa modalità verifica l'esistenza del file di chiave del componente.<br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt> </dl>                                                               | Fornisce il percorso del componente solo se la funzionalità esiste. In caso contrario, restituisce una stringa vuota. Questa modalità controlla la registrazione del componente, ma non verifica l'esistenza del file di chiave del componente.<br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                   | Fornisce il percorso del componente solo se la funzionalità esiste con un parametro InstallState *di msiInstallStateLocal.* In questo modo viene verificata la registrazione del componente, ma non viene verificata l'esistenza del file di chiave del componente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinazione dei flag msiReinstallMode**</dt><dt></dt> </dl> | Chiama [**ReinstallFeature**](installer-reinstallfeature.md) per reinstallare la funzionalità usando questo parametro per il *parametro ReinstallMode* e quindi fornisce il componente .<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo ProvideComponent** combina le funzionalità di [**UseFeature,**](installer-usefeature.md) [**ConfigureFeature**](installer-configurefeature.md)e [**ComponentPath.**](installer-componentpath.md) Il **metodo ProvideComponent** semplifica la sequenza di chiamata, ma incrementa anche il numero di utilizzi e deve essere usato con cautela per evitare conteggi di utilizzo non accurati. Il **metodo ProvideComponent** offre anche una minore flessibilità rispetto a una serie di singole chiamate ai metodi e alle proprietà indicati in precedenza.

Se l'applicazione viene ripristinata da una situazione imprevista, è probabile che l'applicazione abbia già chiamato [**UseFeature**](installer-usefeature.md) e incrementato il numero di utilizzi. In questo caso, l'applicazione deve evitare di incrementare il numero di utilizzi chiamando il [**metodo ConfigureFeature**](installer-configurefeature.md) anziché il **metodo ProvideComponent.**

L'opzione msiInstallModeExisting non può essere usata in combinazione con i flag msiReinstallMode.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




