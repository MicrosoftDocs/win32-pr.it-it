---
description: La proprietà MSIPATCHREMOVE specifica l'elenco di patch da rimuovere durante un'installazione.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: MSIPATCHREMOVE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1259e42bebdbf44473fb92c666cdb764580c2f54321e7f14d0293b1fa9928103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944509"
---
# <a name="msipatchremove-property"></a>MSIPATCHREMOVE - proprietà

La **proprietà MSIPATCHREMOVE** specifica l'elenco di patch da rimuovere durante un'installazione. Le singole patch nell'elenco sono separate da punti e virgola e possono essere rappresentate dal GUID del codice patch o dal percorso completo della patch. La [**funzione MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) e il [**metodo RemovePatches**](installer-removepatches.md) dell'oggetto [Installer](installer-object.md) impostano la **proprietà MSIPATCHREMOVE.**

La **proprietà MSIPATCHREMOVE** può essere impostata nella riga di comando come indicato di seguito per rimuovere una patch.

**msiexec /i A: \\Example.msi MSIPATCHREMOVE=c: \\ patch \\ qfe1.msp;{ 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/qb**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




