---
description: La proprietà riepilogo conteggio pagine contiene la versione minima del programma di installazione richiesta dal pacchetto di installazione.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Proprietà riepilogo conteggio pagine
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329746"
---
# <a name="page-count-summary-property"></a>Proprietà riepilogo conteggio pagine

La proprietà **Riepilogo conteggio pagine** contiene la versione minima del programma di installazione richiesta dal pacchetto di installazione. Per un minimo di Windows Installer 2,0, questa proprietà deve essere impostata sul valore integer 200. Per un minimo di Windows Installer 3,0, questa proprietà deve essere impostata sul valore integer 300. Per un minimo di Windows Installer 3,1, questa proprietà deve essere impostata su 301. Per un minimo di Windows Installer 4,5, questa proprietà deve essere impostata su 405. Per un minimo di Windows Installer 5,0, questa proprietà deve essere impostata su 500.

Per i [pacchetti di Windows Installer a 64 bit](64-bit-windows-installer-packages.md), questa proprietà deve essere impostata sul valore integer 200 o versione successiva. Per i pacchetti di Windows Installer a 64 bit nella piattaforma Arm64, questa proprietà deve essere impostata sul valore integer 500 o versione successiva.

Per un pacchetto di trasformazione, la proprietà **Riepilogo conteggio pagine** contiene la versione minima del programma di installazione necessaria per elaborare la trasformazione. Impostare su un valore maggiore dei due valori delle proprietà di **Riepilogo dei conteggi delle pagine** che appartengono ai database utilizzati per generare la trasformazione.

Per un pacchetto di patch, la proprietà di **Riepilogo di conteggio pagine** è impostata su null.

Questa proprietà di riepilogo è obbligatoria.

Questa proprietà può essere utilizzata per creare un pacchetto che può essere installato solo dalla versione minima o successiva specificata della Windows Installer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




