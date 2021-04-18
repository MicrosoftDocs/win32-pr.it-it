---
description: La proprietà PATCHNEWSUMMARYCOMMENTS aggiorna la proprietà di riepilogo dei commenti di un'installazione amministrativa durante l'applicazione di patch.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: Proprietà PATCHNEWSUMMARYCOMMENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe2bff9613fa5d39ae300e15c3ee816c5c6fce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325719"
---
# <a name="patchnewsummarycomments-property"></a>Proprietà PATCHNEWSUMMARYCOMMENTS

La proprietà **PATCHNEWSUMMARYCOMMENTS** aggiorna la proprietà di [**Riepilogo dei commenti**](comments-summary.md) di un'installazione amministrativa durante l'applicazione di patch. Questa proprietà viene impostata solo da una trasformazione in un file con estensione msp. Il file con estensione msp deve includere una trasformazione che aggiunge questa proprietà alla [tabella delle proprietà](property-table.md) e ne imposta il valore. Il programma di installazione scrive quindi il valore di **PATCHNEWSUMMARYCOMMENTS** nella proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) .

## <a name="remarks"></a>Commenti

Le proprietà [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS** e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) vengono utilizzate per aggiornare le informazioni di riepilogo quando una patch viene installata in un'immagine amministrativa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




