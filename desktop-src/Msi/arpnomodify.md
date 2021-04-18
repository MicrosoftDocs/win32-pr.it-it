---
description: L'impostazione della proprietà ARPNOMODIFY Disabilita la funzionalità di installazione applicazioni nel pannello di controllo che modifica il prodotto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Proprietà ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328026"
---
# <a name="arpnomodify-property"></a>Proprietà ARPNOMODIFY

L'impostazione della proprietà **ARPNOMODIFY** Disabilita la funzionalità di installazione applicazioni nel pannello di controllo che modifica il prodotto. Per Windows 2000, Disabilita il pulsante **modifica** per il prodotto in **Installazione applicazioni** nel **Pannello di controllo**. Nei sistemi operativi precedenti, se si fa clic sul pulsante installazione **applicazioni** , il prodotto viene disinstallato, anziché in modalità di manutenzione.

Se la proprietà **ARPNOMODIFY** è impostata, l' [azione RegisterProduct](registerproduct-action.md) scrive il valore "nomodify" nella chiave del registro di sistema:

**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstalla** \\ **{*codice Product Key*}**

Se la proprietà **ARPNOMODIFY** è impostata e la proprietà [**ARPNOREMOVE**](arpnoremove.md) non è impostata, l'azione RegisterProduct scrive anche il valore UninstallString in questa chiave. Il valore UnistallString è una riga di comando per la rimozione del prodotto, invece della riconfigurazione del prodotto.

## <a name="remarks"></a>Commenti

In Windows 2000, in questo modo il pulsante **Cambia** per il prodotto viene disabilitato in **Installazione applicazioni** del pannello di **controllo**.

Questa proprietà può essere impostata da una trasformazione di personalizzazione per impedire agli utenti di modificare la personalizzazione di un amministratore tramite **Installazione applicazioni**. Questa proprietà ha effetto solo su **Installazione applicazioni**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Esempio di trasformazione della personalizzazione](a-customization-transform-example.md)
</dt> </dl>

 

 




