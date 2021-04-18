---
description: La proprietà ProductID viene impostata sul ProductID completo dopo una convalida corretta. Questo valore viene visualizzato dall'interfaccia utente e usato dall'azione RegisterProduct. In seguito a una convalida corretta, questa proprietà viene impostata dall'azione ValidateProductID o ValidateProductID ControlEvent. si noti che l'interfaccia utente di esempio specifica fornita con SDK come Uisample.msi richiede un valore per ProductID. Se si utilizza questa interfaccia utente, ma non si desidera utilizzare ProductID per convalidare gli identificatori di prodotto, impostare la proprietà ProductID su &\# 0034; none&\# 0034; nella tabella delle proprietà.
ms.assetid: 6af23f2d-b22a-470d-b979-da32776e0007
title: ProductID (proprietà)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf616e2bc34ce70deb5f6b63dba7287002d4fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330619"
---
# <a name="productid-property"></a>ProductID (proprietà)

La proprietà **ProductID** viene impostata sul **ProductID** completo dopo una convalida corretta.

Questo valore viene visualizzato dall'interfaccia utente e usato dall' [azione RegisterProduct](registerproduct-action.md).

In seguito a una convalida corretta, questa proprietà viene impostata dall' [azione ValidateProductID](validateproductid-action.md) o [ValidateProductID ControlEvent](validateproductid-controlevent.md).

Si noti che l'interfaccia utente di esempio specifica fornita con SDK come Uisample.msi richiede un valore per **ProductID**. Se si utilizza questa interfaccia utente, ma non si desidera utilizzare **ProductID** per convalidare gli identificatori di prodotto, impostare la proprietà **ProductID** su "None" nella [tabella delle proprietà](property-table.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




