---
description: La proprietà EXECUTEMODE specifica il modo in cui il programma di installazione esegue gli aggiornamenti del sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Proprietà EXECUTEMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333782"
---
# <a name="executemode-property"></a>Proprietà EXECUTEMODE

La proprietà **EXECUTEMODE** specifica il modo in cui il programma di installazione esegue gli aggiornamenti del sistema. Questa proprietà può essere utile quando è necessario eseguire un'installazione senza modificare effettivamente il sistema. La proprietà può essere impostata su None per disabilitare le operazioni di aggiornamento, ad esempio l'installazione di file e i valori del registro di sistema.

Questa proprietà può avere uno dei due valori seguenti. Il programma di installazione esamina solo la prima lettera del valore e non fa distinzione tra maiuscole e minuscole.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>Nessuno
</dt> <dd>

Non viene apportata alcuna modifica al sistema. Il programma di installazione esegue l'interfaccia utente e quindi esegue una query sul database.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script
</dt> <dd>

Tutte le modifiche apportate al sistema vengono eseguite tramite l'esecuzione dello script. Si tratta della modalità predefinita.

</dd> </dl>

## <a name="default-value"></a>Valore predefinito

Se questa proprietà non è definita, il valore predefinito della modalità di esecuzione è script.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




