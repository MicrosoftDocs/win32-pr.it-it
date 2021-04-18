---
description: La proprietà MSIRMSHUTDOWN determina il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati per consentire l'installazione dell'aggiornamento.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Proprietà MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331079"
---
# <a name="msirmshutdown-property"></a>Proprietà MSIRMSHUTDOWN

La proprietà **MSIRMSHUTDOWN** determina il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati per consentire l'installazione dell'aggiornamento.

## <a name="value"></a>Valore



| Valore                                                                        | Significato                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | I processi o i servizi che attualmente utilizzano i file interessati dall'aggiornamento vengono arrestati.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | I processi o i servizi che attualmente utilizzano i file interessati dall'aggiornamento e che non rispondono a [Gestione riavvio](../rstmgr/restart-manager-portal.md)sono costretti ad arrestarsi.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | I processi o i servizi che attualmente utilizzano i file interessati dall'aggiornamento vengono arrestati solo se sono stati registrati per un riavvio. Se un processo o un servizio non è stato registrato per il riavvio, non vengono arrestati processi o servizi.<br/> |



 

## <a name="remarks"></a>Commenti

La proprietà **MSIRMSHUTDOWN** viene ignorata se [Gestione riavvio](../rstmgr/restart-manager-portal.md) non è disponibile o è disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Per informazioni sul Service Pack minimo richiesto da una versione Windows Installer, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
