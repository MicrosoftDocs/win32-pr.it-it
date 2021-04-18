---
description: Il Windows SDK contiene un'utilità da riga di comando, Sc.exe, che può essere utilizzata per eseguire query o modificare il database dei servizi installati. I relativi comandi corrispondono alle funzioni fornite da SCM. La sintassi è la seguente.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Configurazione di un servizio con SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306339"
---
# <a name="configuring-a-service-using-sc"></a>Configurazione di un servizio con SC

Il Windows SDK contiene un'utilità da riga di comando, Sc.exe, che può essere utilizzata per eseguire query o modificare il database dei servizi installati. I relativi comandi corrispondono alle funzioni fornite da SCM. La sintassi è la seguente.

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

<dl> <dd>boot</dd> <dd>config</dd> <dd>create</dd> <dd>eliminare</dd> <dd>description</dd> <dd>EnumDepend</dd> <dd>operazione non riuscita</dd> <dd>failureflag</dd> <dd>GetDisplayName</dd> <dd>GetKeyName</dd> <dd>Lock</dd> <dd>qc</dd> <dd>qdescription</dd> <dd>qfailure</dd> <dd>qfailureflag</dd> <dd>qprivs</dd> <dd>qsidtype</dd> <dd>query</dd> <dd>queryex</dd> <dd>privs</dd> <dd>QueryLock</dd> <dd>sdset</dd> <dd>sdshow</dd> <dd>showsid</dd> <dd>SIDType</dd> </dl> </dd> <dt>

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

[Configurazione del servizio](service-configuration.md)
</dt> <dt>

[Installazione, rimozione ed enumerazione del servizio](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



