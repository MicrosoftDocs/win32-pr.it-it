---
description: La proprietà MSIDISABLERMRESTART determina il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati e riavviati per consentire l'installazione dell'aggiornamento.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Proprietà MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329341"
---
# <a name="msidisablermrestart-property"></a>Proprietà MSIDISABLERMRESTART

La proprietà **MSIDISABLERMRESTART** determina il modo in cui le applicazioni o i servizi che attualmente utilizzano i file interessati da un aggiornamento devono essere arrestati e riavviati per consentire l'installazione dell'aggiornamento.

## <a name="value"></a>Valore



| Valore                                                                        | Significato                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Tutti i servizi di sistema arrestati per installare l'aggiornamento vengono riavviati. Tutte le applicazioni registrate con [Gestione riavvio](../rstmgr/restart-manager-portal.md) vengono riavviate.<br/> |
| <dl> <dt>1</dt> </dl> | I processi arrestati utilizzando [Gestione riavvio](../rstmgr/restart-manager-portal.md) durante l'installazione dell'aggiornamento non verranno riavviati dopo l'applicazione dell'aggiornamento.<br/>                           |



 

## <a name="remarks"></a>Commenti

La proprietà **MSIDISABLERMRESTART** viene ignorata se [Gestione riavvio](../rstmgr/restart-manager-portal.md) non è disponibile o è disabilitato.

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

 

 
