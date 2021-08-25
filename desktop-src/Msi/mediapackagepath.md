---
description: "Se il pacchetto di installazione che viene caricato con un'applicazione non si trova nella radice del CD-ROM ricevuto dai clienti, la proprietà MEDIAPACKAGEPATH deve essere impostata nella riga di comando sul percorso relativo dell'applicazione nel CD-ROM. Ad esempio, se il percorso del pacchetto nel supporto è E: \\\\ MyPathMy.msi, usare \\\\ MEDIAPACKAGEPATH=&\\# 0034; \\\\ MyPath \\\\ & \\# 0034;. Gli amministratori possono creare CD-ROMs da un punto di installazione amministrativa. Se il percorso della radice dell'installazione viene modificato nei nuovi CD-ROM, la proprietà MEDIAPACKAGEPATH deve essere impostata sul nuovo percorso per l'installazione da questo supporto. Un'origine con un percorso sul CD-ROM diverso da quello specificato nel pacchetto non è utilizzabile. Non è tuttavia necessario usare questa proprietà quando si crea un punto di installazione amministrativa dai supporti di spedizione."
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: MEDIAPACKAGEPATH - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140afc253e27b3c861f941e88b55f84ad49f43984fcc3a5aaf82d06fe414e6a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926881"
---
# <a name="mediapackagepath-property"></a>MEDIAPACKAGEPATH - proprietà

Se il pacchetto di installazione che viene caricato con un'applicazione non si trova nella radice del CD-ROM ricevuto dai clienti, la proprietà **MEDIAPACKAGEPATH** deve essere impostata nella riga di comando sul percorso relativo dell'applicazione nel CD-ROM.

Ad esempio, se il percorso del pacchetto nel supporto è E: \\ MyPathMy.msi, usare \\ MEDIAPACKAGEPATH=" \\ MyPath \\ ".

Gli amministratori possono creare CD-ROMs da un punto di installazione amministrativa. Se il percorso della radice dell'installazione viene modificato nei nuovi CD-ROM, la proprietà **MEDIAPACKAGEPATH** deve essere impostata sul nuovo percorso per l'installazione da questo supporto. Un'origine con un percorso sul CD-ROM diverso da quello specificato nel pacchetto non è utilizzabile. Non è tuttavia necessario usare questa proprietà quando si crea un punto di installazione amministrativa dai supporti di spedizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




