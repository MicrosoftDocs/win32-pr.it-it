---
description: La proprietà Riepilogo conteggio pagine contiene la versione minima del programma di installazione richiesta dal pacchetto di installazione.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Proprietà Riepilogo conteggio pagine
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690f19db5b8b4dc4dff3c3eb30f616803754bfac199a3aa1e6656da0f1e3fa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145414"
---
# <a name="page-count-summary-property"></a>Proprietà Riepilogo conteggio pagine

La **proprietà Riepilogo conteggio** pagine contiene la versione minima del programma di installazione richiesta dal pacchetto di installazione. Per un minimo di Windows Installer 2.0, questa proprietà deve essere impostata sul numero intero 200. Per un minimo di Windows Installer 3.0, questa proprietà deve essere impostata sul numero intero 300. Per un minimo di Windows Installer 3.1, questa proprietà deve essere impostata su 301. Per un minimo di Windows Installer 4.5, questa proprietà deve essere impostata su 405. Per un minimo di Windows Installer 5.0, questa proprietà deve essere impostata su 500.

Per [i pacchetti di Windows a 64 bit,](64-bit-windows-installer-packages.md)questa proprietà deve essere impostata sul numero intero 200 o superiore. Per i pacchetti di Windows a 64 bit nella piattaforma Arm64, questa proprietà deve essere impostata sul numero intero 500 o superiore.

Per un pacchetto di trasformazione, la **proprietà Riepilogo conteggio** pagine contiene la versione minima del programma di installazione necessaria per elaborare la trasformazione. Impostare sul valore maggiore dei due valori della proprietà **Riepilogo** conteggio pagine che appartengono ai database usati per generare la trasformazione.

Per un pacchetto patch, la **proprietà Riepilogo conteggio** pagine è impostata su Null.

Questa proprietà di riepilogo è obbligatoria.

Questa proprietà può essere usata per creare un pacchetto che può essere installato solo dalla versione minima o successiva specificata del Windows installer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




