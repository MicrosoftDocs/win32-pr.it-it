---
description: Il Windows SDK contiene un'utilità da riga di comando, Sc.exe, che può essere utilizzata per controllare un servizio. I relativi comandi corrispondono alle funzioni fornite da SCM. La sintassi è la seguente.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controllo di un servizio con SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316616"
---
# <a name="controlling-a-service-using-sc"></a>Controllo di un servizio con SC

Il Windows SDK contiene un'utilità da riga di comando, Sc.exe, che può essere utilizzata per controllare un servizio. I relativi comandi corrispondono alle funzioni fornite da SCM. La sintassi è la seguente.

## <a name="syntax"></a>Sintassi

**SC** \[ *Nomeserver* \] *Comando* \[ *ServiceName* \] \[  \] opzione1 \[ *opzione2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Nomeserver*
</dt> <dd>

Nome del server facoltativo. Utilizzare il formato \\ \\ *ServerName*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Comando*
</dt> <dd>

Uno dei comandi seguenti:

<dl> <dd>continue</dd> <dd>controllo</dd> <dd>interrogare</dd> <dd>Sospendi</dd> <dd>start</dd> <dd>stop</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*
</dt> <dd>

Nome del servizio, come specificato al momento dell'installazione.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*opzione1*
</dt> <dd>

Parametro opzionale.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*opzione2*
</dt> <dd>

Parametro opzionale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per visualizzare la sintassi completa per un comando, usare il comando seguente:

**SC** ( *comando* )

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richieste di controllo del servizio](service-control-requests.md)
</dt> <dt>

[Avvio del servizio](service-startup.md)
</dt> </dl>

 

 



