---
description: L'impostazione della proprietà ARPNOREMOVE disabilita la funzionalità Installazione applicazioni Pannello di controllo che rimuove il prodotto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: ARPNOREMOVE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d69e066aeb96861be220a40334d44bf55fe0569e855029d2a19399b56a1c205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105431"
---
# <a name="arpnoremove-property"></a>ARPNOREMOVE - proprietà

**L'impostazione della proprietà ARPNOREMOVE** disabilita la funzionalità Installazione applicazioni  **Pannello di controllo** che rimuove il prodotto. Ad Windows 2000, il pulsante  Rimuovi per il prodotto viene disabilitato da Installazione applicazioni **in** **Pannello di controllo**. Per i sistemi operativi precedenti, ciò ha l'effetto di rimuovere il prodotto dall'elenco di prodotti installati in Installazione applicazioni **in** **Pannello di controllo**.

Se la **proprietà ARPNOREMOVE** è impostata, l'azione [RegisterProduct](registerproduct-action.md) scrive il valore "NoRemove" nella chiave del Registro di sistema:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstallare** \\ **{*codice Product Key*}**

**L'impostazione della proprietà ARPNOREMOVE** impedisce la scrittura del valore UninstallString in questa chiave. Il valore UnistallString è una riga di comando per rimuovere il prodotto, anziché riconfigurare il prodotto.

## <a name="remarks"></a>Commenti

Ad esempio, questa proprietà può essere impostata durante una trasformazione di personalizzazione per impedire agli utenti di rimuovere una personalizzazione dell'amministratore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 o versione successiva Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




