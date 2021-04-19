---
description: La proprietà MSIPATCHREMOVE specifica l'elenco di patch da rimuovere durante un'installazione.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Proprietà MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326266"
---
# <a name="msipatchremove-property"></a>Proprietà MSIPATCHREMOVE

La proprietà **MSIPATCHREMOVE** specifica l'elenco di patch da rimuovere durante un'installazione. Le singole patch nell'elenco sono separate da punti e virgola e possono essere rappresentate dal GUID del codice della patch o dal percorso completo della patch. La funzione [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) e il metodo [**RemovePatches**](installer-removepatches.md) dell'oggetto [Installer](installer-object.md) impostano la proprietà **MSIPATCHREMOVE** .

Per rimuovere una patch, è possibile impostare la proprietà **MSIPATCHREMOVE** nella riga di comando come indicato di seguito.

**msiexec/i A: \\Example.msi MSIPATCHREMOVE = c: \\ patches \\ QFE1. msp; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




