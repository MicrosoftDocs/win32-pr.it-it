---
description: La presenza della proprietà MSIINSTANCEGUID indica che un codice prodotto&\# 8211; la modifica della trasformazione è registrata nel prodotto.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Proprietà MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325462"
---
# <a name="msiinstanceguid-property"></a>Proprietà MSIINSTANCEGUID

La presenza della proprietà **MSIINSTANCEGUID** indica che nel prodotto è registrata una trasformazione che modifica il codice del prodotto. Il valore della proprietà **MSIINSTANCEGUID** specifica quale istanza di un prodotto deve essere utilizzata per l'installazione. La proprietà **MSIINSTANCEGUID** può fare riferimento solo a un prodotto che è già stato installato con una trasformazione istanza.

Le trasformazioni dell'istanza sono codice del prodotto: modifica delle trasformazioni disponibili con il programma di installazione in esecuzione in Windows Server 2003 o Windows XP. Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




