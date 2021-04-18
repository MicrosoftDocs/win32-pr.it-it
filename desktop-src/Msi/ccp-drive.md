---
description: La \_ proprietà dell'unità CCP è impostata sul percorso radice del volume rimovibile che deve essere cercato da RMCCPSearch.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: Proprietà CCP_DRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327326"
---
# <a name="ccp_drive-property"></a>\_Proprietà unità CCP

La proprietà dell' **\_ unità CCP** è impostata sul percorso radice del volume rimovibile che deve essere cercato da [RMCCPSearch](rmccpsearch-action.md). L'azione RMCCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.

Questa proprietà viene in genere impostata tramite l'interfaccia utente o un'azione personalizzata. Questa proprietà deve essere impostata prima dell'esecuzione dell'azione [RMCCPSearch](rmccpsearch-action.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




