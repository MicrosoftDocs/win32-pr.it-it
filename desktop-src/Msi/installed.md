---
description: La proprietà installata è impostata solo se il prodotto è installato per computer o per l'utente corrente.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Proprietà installata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330284"
---
# <a name="installed-property"></a>Proprietà installata

La proprietà **installata** è impostata solo se il prodotto è installato per computer o per l'utente corrente. Questa proprietà non viene impostata se il prodotto è installato per un utente diverso.

La proprietà **installata** può essere utilizzata nelle espressioni condizionali per determinare se un prodotto è installato per computer o per l'utente corrente. La proprietà, ad esempio, può essere utilizzata nella colonna condizionale di una tabella di sequenza o per distinguere tra una prima installazione e un'installazione di manutenzione.

Per determinare se il prodotto è installato per un utente diverso, controllare la proprietà [**ProductState**](productstate.md) .

Il valore della proprietà [**ProductVersion**](productversion.md) è la versione del prodotto in formato stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




