---
description: Il metodo ReinstallFeature dell'oggetto Installer reinstalla le funzionalità o corregge i problemi relativi alle funzionalità installate.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Metodo Installer.ReinstallFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dfe4cb96ccac85fb5b94f3a2a8ec3dcca48f6fa4300a6bceb338b2ebbe01da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946287"
---
# <a name="installerreinstallfeature-method"></a>Metodo Installer.ReinstallFeature

Il **metodo ReinstallFeature** dell'oggetto [**Installer**](installer-object.md) reinstalla le funzionalità o corregge i problemi relativi alle funzionalità installate.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
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

Specifica la funzionalità da reinstallare. La funzionalità padre o figlio della funzionalità specificata non viene reinstallata. Per reinstallare la funzionalità padre o figlio, è necessario chiamare il **metodo ReinstallFeature** per ogni funzionalità separatamente o usare il [**metodo ReinstallProduct.**](installer-reinstallproduct.md)

</dd> <dt>

*ReinstallMode* 
</dt> <dd>

Specifica il tipo di reinstallazione. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                    | Significato                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <dt>**msiReinstallModeFileMissing**</dt> </dl>                     | Reinstalla solo se il file non è presente.<br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <dt>**msiReinstallModeFileOlderVersion**</dt> </dl> | Reinstalla se il file è mancante o è una versione precedente.<br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <dt>**msiReinstallModeFileEqualVersion**</dt> </dl> | Reinstalla se il file è mancante o è una versione uguale o precedente.<br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <dt>**msiReinstallModeFileExact**</dt> </dl>                             | Reinstalla se il file è mancante o non è una versione esatta.<br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <dt>**msiReinstallModeFileVerify**</dt> </dl>                         | Controlla la somma dei file eseguibili e reinstalla se sono mancanti o danneggiati.<br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <dt>**msiReinstallModeFileReplace**</dt> </dl>                     | Reinstalla tutti i file indipendentemente dalla versione.<br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <dt>**msiReinstallModeUserData**</dt> </dl>                                 | Garantisce le voci del Registro di sistema per=user obbligatorie.<br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <dt>**msiReinstallModeMachineData**</dt> </dl>                     | Garantisce le voci obbligatorie del Registro di sistema per=computer.<br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <dt>**msiReinstallModeShortcut**</dt> </dl>                                 | Convalida i tasti di scelta rapida.<br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <dt>**msiReinstallModePackage**</dt> </dl>                                     | Usa l'origine recache per installare il pacchetto.<br/>                        |



 

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

[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[Funzioni di installazione e configurazione](installer-function-reference.md)
</dt> </dl>

 

 




