---
description: "Se il pacchetto di installazione distribuito con un'applicazione non è alla radice del CD-ROM che i clienti ricevono, è necessario impostare la proprietà MEDIAPACKAGEPATH nella riga di comando sul percorso relativo dell'applicazione sul CD-ROM. Se, ad esempio, il percorso del pacchetto nel supporto è E: \\\\ percorso \\\\My.msi, utilizzare MEDIAPACKAGEPATH =&\\# 0034; \\\\ Percorso \\\\ & \\# 0034;. Gli amministratori possono creare CD-ROMs da un punto di installazione amministrativa. Se il percorso della radice dell'installazione viene modificato nei nuovi CD-ROM, la proprietà MEDIAPACKAGEPATH deve essere impostata sul nuovo percorso da installare da questo supporto. Un'origine con un percorso su CD-ROM diverso da quello specificato nel pacchetto è inutilizzabile. Tuttavia, non è necessario utilizzare questa proprietà quando si crea un punto di installazione amministrativa da supporti di spedizione."
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Proprietà MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329618"
---
# <a name="mediapackagepath-property"></a>Proprietà MEDIAPACKAGEPATH

Se il pacchetto di installazione distribuito con un'applicazione non è alla radice del CD-ROM che i clienti ricevono, è necessario impostare la proprietà **MEDIAPACKAGEPATH** nella riga di comando sul percorso relativo dell'applicazione sul CD-ROM.

Se, ad esempio, il percorso del pacchetto nel supporto è E: \\ percorso \\My.msi, utilizzare MEDIAPACKAGEPATH = " \\ percorso \\ ".

Gli amministratori possono creare CD-ROMs da un punto di installazione amministrativa. Se il percorso della radice dell'installazione viene modificato nei nuovi CD-ROM, la proprietà **MEDIAPACKAGEPATH** deve essere impostata sul nuovo percorso da installare da questo supporto. Un'origine con un percorso su CD-ROM diverso da quello specificato nel pacchetto è inutilizzabile. Tuttavia, non è necessario utilizzare questa proprietà quando si crea un punto di installazione amministrativa da supporti di spedizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




