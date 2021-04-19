---
description: Impostare la proprietà MSIUSEREALADMINDETECTION su 1 per richiedere al programma di installazione di utilizzare le informazioni utente effettive durante l'impostazione della proprietà AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Proprietà MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331067"
---
# <a name="msiuserealadmindetection-property"></a>Proprietà MSIUSEREALADMINDETECTION

Impostare la proprietà **MSIUSEREALADMINDETECTION** su 1 per richiedere al programma di installazione di utilizzare le informazioni utente effettive durante l'impostazione della proprietà [**AdminUser**](adminuser.md) . Quando è in esecuzione in Windows Vista, i [**privilegi**](privileged.md) e **AdminUser** sono gli stessi. Gli autori devono utilizzare la proprietà **Privileged** nei nuovi pacchetti. I pacchetti legacy che richiedono proprietà con **privilegi** e **AdminUser** distinti possono ripristinare la differenza impostando la proprietà **MSIUSEREALADMINDETECTION** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




