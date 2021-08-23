---
description: La proprietà MSIRMSHUTDOWN determina il modo in cui le applicazioni o i servizi che attualmente usano i file interessati da un aggiornamento devono essere arrestati per abilitare l'installazione dell'aggiornamento.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: MSIRMSHUTDOWN - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac31a924727217ac86937f4f7ac553717138461e0668a7e79916ffab796f8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012879"
---
# <a name="msirmshutdown-property"></a>MSIRMSHUTDOWN - proprietà

La **proprietà MSIRMSHUTDOWN** determina il modo in cui le applicazioni o i servizi che attualmente usano i file interessati da un aggiornamento devono essere arrestati per abilitare l'installazione dell'aggiornamento.

## <a name="value"></a>Valore



| Valore                                                                        | Significato                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | I processi o i servizi che attualmente usano i file interessati dall'aggiornamento vengono arrestati.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | I processi o i servizi che attualmente usano i file interessati dall'aggiornamento e che non rispondono a Gestione riavvio [devono](../rstmgr/restart-manager-portal.md)essere arrestati.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | I processi o i servizi che attualmente usano i file interessati dall'aggiornamento vengono arrestati solo se sono stati tutti registrati per un riavvio. Se un processo o un servizio non è stato registrato per un riavvio, non vengono arrestati processi o servizi.<br/> |



 

## <a name="remarks"></a>Commenti

La **proprietà MSIRMSHUTDOWN viene** ignorata se Gestione [riavvio](../rstmgr/restart-manager-portal.md) non è disponibile o è disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Per informazioni Windows service pack minimo richiesto [Run-Time da](windows-installer-portal.md) una versione Windows Installer, vedere i requisiti di Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
