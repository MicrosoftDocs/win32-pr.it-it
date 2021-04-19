---
description: La proprietà MSINEWINSTANCE indica l'installazione di una nuova istanza di un prodotto con le trasformazioni dell'istanza.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Proprietà MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330153"
---
# <a name="msinewinstance-property"></a>Proprietà MSINEWINSTANCE

La proprietà **MSINEWINSTANCE** indica l'installazione di una nuova istanza di un prodotto con le trasformazioni dell'istanza. Questa proprietà supporta più istanze tramite codice del prodotto: modifica delle trasformazioni. Il valore di questa proprietà è 1. Per la presenza di questa proprietà nella riga di comando è necessario che sia presente anche la proprietà [**TRANSformations**](transforms.md) . La prima trasformazione elencata in **TRASformazioni** deve essere una trasformazione dell'istanza. Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md)

Questa proprietà è disponibile con il programma di installazione che esegue un sistema in Windows Server 2003 o Windows XP.

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

 

 




