---
description: L'impostazione della proprietà ARPNOREMOVE Disabilita la funzionalità Installazione applicazioni nel pannello di controllo che consente di rimuovere il prodotto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Proprietà ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328020"
---
# <a name="arpnoremove-property"></a>Proprietà ARPNOREMOVE

L'impostazione della proprietà **ARPNOREMOVE** Disabilita la funzionalità **Installazione applicazioni** nel **Pannello di controllo** che consente di rimuovere il prodotto. Per Windows 2000, Disabilita il pulsante **Rimuovi** per il prodotto da **Installazione applicazioni** nel **Pannello di controllo**. Per i sistemi operativi precedenti, ciò comporta la rimozione del prodotto dall'elenco dei prodotti installati in installazione **applicazioni** nel **Pannello di controllo**.

Se la proprietà **ARPNOREMOVE** è impostata, l' [azione RegisterProduct](registerproduct-action.md) scrive il valore "NoRemove" nella chiave del registro di sistema:

**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstalla** \\ **{*codice Product Key*}**

L'impostazione della proprietà **ARPNOREMOVE** impedisce la scrittura del valore UninstallString sotto questa chiave. Il valore UnistallString è una riga di comando per la rimozione del prodotto, invece della riconfigurazione del prodotto.

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata, ad esempio, durante una trasformazione di personalizzazione per impedire agli utenti di rimuovere una personalizzazione di amministratore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 o versione successiva in Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




