---
description: La proprietà ProductID viene impostata sull'intero ProductID dopo una convalida riuscita. Questo valore viene visualizzato dall'interfaccia utente e usato dall'azione RegisterProduct. Dopo una convalida riuscita, questa proprietà viene impostata dall'azione ValidateProductID o da ValidateProductID ControlEvent. Si noti che la particolare interfaccia utente di esempio fornita con l'SDK come Uisample.msi richiede un valore per ProductID. Se si usa questa interfaccia utente, ma non si vuole usare ProductID per convalidare gli identificatori di prodotto, impostare la proprietà ProductID su &\# 0034;none&\# 0034; nella tabella Property.
ms.assetid: 6af23f2d-b22a-470d-b979-da32776e0007
title: ProductID - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e737f5c6c2b007709ed21c5950e93f9f3cb7b08315fbf7871d1a8855ee075
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074701"
---
# <a name="productid-property"></a>ProductID - proprietà

La **proprietà ProductID** viene impostata sull'intero **ProductID dopo** una convalida riuscita.

Questo valore viene visualizzato dall'interfaccia utente e usato [dall'azione RegisterProduct](registerproduct-action.md).

Dopo una convalida riuscita, questa proprietà viene impostata dall'azione [ValidateProductID](validateproductid-action.md) o [da ValidateProductID ControlEvent.](validateproductid-controlevent.md)

Si noti che l'interfaccia utente di esempio specifica fornita con l'SDK Uisample.msi richiede un valore per **ProductID**. Se si usa questa interfaccia utente, ma non si vuole usare **ProductID** per convalidare gli identificatori di prodotto, impostare la **proprietà ProductID** su "none" nella [tabella Property](property-table.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




