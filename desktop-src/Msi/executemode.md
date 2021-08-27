---
description: La proprietà EXECUTEMODE specifica la modalità di esecuzione degli aggiornamenti di sistema da parte del programma di installazione.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: EXECUTEMODE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 750b6c3a20ab05388fcd6926463dde8259440bd6087306b1bf0cc1a6c387cd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082871"
---
# <a name="executemode-property"></a>EXECUTEMODE - proprietà

La **proprietà EXECUTEMODE** specifica la modalità di esecuzione degli aggiornamenti di sistema da parte del programma di installazione. Questa proprietà può essere utile quando è necessario eseguire un'installazione senza modificare effettivamente il sistema. La proprietà può essere impostata su None per disabilitare le operazioni di aggiornamento, ad esempio l'installazione di file e valori del Registro di sistema.

Questa proprietà può avere uno dei due valori seguenti. Il programma di installazione esamina solo la prima lettera del valore e non fa distinzione tra maiuscole e minuscole.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>Nessuno
</dt> <dd>

Non vengono apportate modifiche al sistema. Il programma di installazione esegue l'interfaccia utente e quindi esegue una query sul database.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>copione
</dt> <dd>

Tutte le modifiche al sistema vengono apportate tramite l'esecuzione di script. Si tratta della modalità predefinita.

</dd> </dl>

## <a name="default-value"></a>Valore predefinito

Se questa proprietà non è definita, per impostazione predefinita la modalità di esecuzione è Script.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




