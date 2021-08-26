---
description: La proprietà MSINEWINSTANCE indica l'installazione di una nuova istanza di un prodotto con trasformazioni di istanza.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: MSINEWINSTANCE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b26831f1171813d9df9e2c4124a4d6c24ea7efbf707fc5c15eefc9d6a8b1046
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082851"
---
# <a name="msinewinstance-property"></a>MSINEWINSTANCE - proprietà

La **proprietà MSINEWINSTANCE** indica l'installazione di una nuova istanza di un prodotto con trasformazioni di istanza. Questa proprietà supporta più istanze tramite trasformazioni di modifica del codice prodotto. Il valore di questa proprietà è 1. La presenza di questa proprietà nella riga di comando richiede che sia presente anche la proprietà [**TRANSFORMS.**](transforms.md) La prima trasformazione elencata in **TRANSFORMS** deve essere una trasformazione di istanza. Per altre informazioni, [vedere Installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md)

Questa proprietà è disponibile con il programma di installazione che esegue un sistema nel Windows Server 2003 o Windows XP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




