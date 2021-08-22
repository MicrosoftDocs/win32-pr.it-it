---
description: L'impostazione della proprietà ARPNOMODIFY disabilita la funzionalità Installazione applicazioni Pannello di controllo che modifica il prodotto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: ARPNOMODIFY - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c9a097f183c13e1c5b6f8f8b6a521c8a03149df130befaa1221b14b732418a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581811"
---
# <a name="arpnomodify-property"></a>ARPNOMODIFY - proprietà

**L'impostazione della proprietà ARPNOMODIFY** disabilita la funzionalità Installazione applicazioni Pannello di controllo che modifica il prodotto. Per Windows 2000, il pulsante  Modifica per il prodotto viene disabilitato **in** Installazione applicazioni in **Pannello di controllo**. Nei sistemi operativi precedenti fare clic sul pulsante **Installazione** applicazioni per disinstallare il prodotto anziché accedere alla procedura guidata per la modalità manutenzione.

Se la **proprietà ARPNOMODIFY è** impostata, l'azione [RegisterProduct](registerproduct-action.md) scrive il valore "NoModify" nella chiave del Registro di sistema:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstallare** \\ **{*codice Product Key*}**

Se la **proprietà ARPNOMODIFY** è impostata e la proprietà [**ARPNOREMOVE**](arpnoremove.md) non è impostata, l'azione RegisterProduct scrive anche il valore UninstallString in questa chiave. Il valore UnistallString è una riga di comando per rimuovere il prodotto, anziché riconfigurare il prodotto.

## <a name="remarks"></a>Commenti

In Windows 2000 il pulsante Cambia  per il prodotto  viene disabilitato in Installazione applicazioni **del Pannello di controllo**.

Questa proprietà può essere impostata da una trasformazione di personalizzazione per impedire agli utenti di modificare la personalizzazione di un amministratore **tramite Installazione applicazioni.** Questa proprietà influisce **solo su Installazione applicazioni.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Esempio di trasformazione di personalizzazione](a-customization-transform-example.md)
</dt> </dl>

 

 




