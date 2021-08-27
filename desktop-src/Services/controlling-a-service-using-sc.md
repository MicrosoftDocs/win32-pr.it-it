---
description: L Windows SDK contiene un'utilità della riga di comando, Sc.exe, che può essere usata per controllare un servizio. I comandi corrispondono alle funzioni fornite da Gestione controllo servizi. La sintassi è la seguente.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controllo di un servizio tramite SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2481e0d13f19760c042d39efe4ec6094a3ef270312aeb31d2228d401d914bc1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126451"
---
# <a name="controlling-a-service-using-sc"></a>Controllo di un servizio tramite SC

L Windows SDK contiene un'utilità della riga di comando, Sc.exe, che può essere usata per controllare un servizio. I comandi corrispondono alle funzioni fornite da Gestione controllo servizi. La sintassi è la seguente.

## <a name="syntax"></a>Sintassi

**sc** \[ *NomeServer* \] *Comando* \[ *ServiceName* \] \[ *opzione1* \] \[ *opzione 2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Nomeserver*
</dt> <dd>

Nome del server facoltativo. Usare il formato \\ \\ *ServerName*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Comando*
</dt> <dd>

Uno dei comandi seguenti:

<dl> <dd>continue</dd> <dd>controllo</dd> <dd>Interrogare</dd> <dd>Sospendi</dd> <dd>Avvio</dd> <dd>stop</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Servicename*
</dt> <dd>

Nome del servizio, come specificato al momento dell'installazione.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*opzione1*
</dt> <dd>

Parametro opzionale.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*opzione 2*
</dt> <dd>

Parametro opzionale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per visualizzare la sintassi completa per un comando, usare il comando seguente:

**Comando sc** 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richieste di controllo del servizio](service-control-requests.md)
</dt> <dt>

[Avvio del servizio](service-startup.md)
</dt> </dl>

 

 



