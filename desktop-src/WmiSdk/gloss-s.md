---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 223cfe51-8b1d-4965-b7b1-acc3cd5619f0
ms.tgt_platform: multiple
title: S (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48473c58a1c9aae3f3c9e67f7723167b46df0285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318194"
---
# <a name="s-wmi"></a>S (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [d](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) S [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_schema"></span><span id="WMI.GLOSS_SCHEMA"></span>**Schema**
</dt> <dd>

Raccolta di definizioni di classe che descrivono [*oggetti gestiti*](gloss-m.md) in un ambiente specifico.

</dd> <dt>

<span id="wmi.gloss_security_descriptor"></span><span id="WMI.GLOSS_SECURITY_DESCRIPTOR"></span>**descrittore di sicurezza**
</dt> <dd>

Struttura di dati che contiene le informazioni di sicurezza per un oggetto a protezione diretta, ad esempio una condivisione, un file, un sink o un filtro eventi.

</dd> <dt>

<span id="wmi.gloss_security_identifier"></span><span id="WMI.GLOSS_SECURITY_IDENTIFIER"></span>**ID di sicurezza (SID)**
</dt> <dd>

Struttura di dati che identifica gli account utente, gruppo e computer.

</dd> <dt>

<span id="wmi.gloss_semi_synchronous"></span><span id="WMI.GLOSS_SEMI_SYNCHRONOUS"></span>**semi sincrono**
</dt> <dd>

Vedere il *metodo semisincrono*.

</dd> <dt>

<span id="wmi.gloss_semi__synchronous"></span><span id="WMI.GLOSS_SEMI__SYNCHRONOUS"></span>**semi-sincrono**
</dt> <dd>

Vedere il *metodo semisincrono*.

</dd> <dt>

<span id="wmi.gloss_semisynchronous"></span><span id="WMI.GLOSS_SEMISYNCHRONOUS"></span>**metodo semisincrono**
</dt> <dd>

Chiamata al metodo che restituisce immediatamente e consente all'applicazione o allo script di enumerare gli oggetti restituiti come raccolta.

</dd> <dt>

<span id="gloss_servicesid"></span><span id="GLOSS_SERVICESID"></span>**SID servizio**
</dt> <dd>

*SID* univoco creato per ogni contesto di sicurezza. ovvero uno per "LocalService" e uno per "NetworkService". Solo il *SID del servizio* dispone delle autorizzazioni per le risorse, ad esempio i thread e gli eventi, creati dal processo host del provider WMI (wmiprvse.exe).

</dd> <dt>

<span id="wmi.gloss_sid"></span><span id="WMI.GLOSS_SID"></span>**SID**
</dt> <dd>

Vedere *identificatore di sicurezza*.

</dd> <dt>

<span id="wmi.gloss_singleton_class"></span><span id="WMI.GLOSS_SINGLETON_CLASS"></span>**classe singleton**
</dt> <dd>

Classe WMI che supporta una sola istanza.

</dd> <dt>

<span id="wmi.gloss_sink"></span><span id="WMI.GLOSS_SINK"></span>**sink**
</dt> <dd>

Oggetto COM che funge da destinazione di recapito fisica per i risultati di un'operazione asincrona o di una notifica degli eventi. Un sink implementato da un [*consumer permanente*](gloss-p.md) supporta l'interfaccia [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Un sink implementato da un [*consumer temporaneo*](gloss-t.md) o da applicazioni che effettuano chiamate asincrone supporta l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .

I client di scripting possono usare l'oggetto e gli eventi [**SWbemSink**](swbemsink.md) , ad esempio [**OnObjectReady**](swbemsink-onobjectready.md), per ricevere callback derivanti da chiamate asincrone.

</dd> <dt>

<span id="wmi.gloss_standard_consumer"></span><span id="WMI.GLOSS_STANDARD_CONSUMER"></span>**consumer standard**
</dt> <dd>

[*Utenti permanenti*](gloss-p.md) preinstallati che eseguono un'azione, ad esempio l'invio di un messaggio di posta elettronica o la scrittura in un log se configurati da un file [*Managed Object Format (MOF)*](gloss-m.md) o uno script.

</dd> <dt>

<span id="wmi.gloss_standard_provider"></span><span id="WMI.GLOSS_STANDARD_PROVIDER"></span>**provider standard**
</dt> <dd>

[*Provider*](gloss-p.md) integrato in WMI, che è diverso da un provider personalizzato o di terze parti.

</dd> <dt>

<span id="wmi.gloss_standard_qualifier"></span><span id="WMI.GLOSS_STANDARD_QUALIFIER"></span>**qualificatore standard**
</dt> <dd>

[*Qualificatore*](gloss-q.md) che l' [*CIM Object Manager*](gloss-c.md) si connette automaticamente a una classe, un'istanza, una proprietà, un metodo o un parametro di un metodo.

</dd> <dt>

<span id="wmi.gloss_standard_schema"></span><span id="WMI.GLOSS_STANDARD_SCHEMA"></span>**schema standard**
</dt> <dd>

Framework concettuale comune che organizza e mette in correlazione le classi che rappresentano lo stato operativo corrente di un sistema, una rete o un'applicazione. [*Distributed Management Task Force (DMTF)*](gloss-d.md) definisce lo schema standard nel [*Common Information Model (CIM)*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_static_class"></span><span id="WMI.GLOSS_STATIC_CLASS"></span>**classe statica**
</dt> <dd>

Una definizione di classe CIM che cambia raramente e viene archiviata nel [*repository CIM*](gloss-c.md) fino a quando non viene eliminata in modo esplicito. Il [*CIM Object Manager*](gloss-c.md) può fornire una definizione di una classe statica senza un [*provider*](gloss-p.md). Una classe statica può supportare istanze *statiche* o [*dinamiche*](gloss-d.md).

</dd> <dt>

<span id="wmi.gloss_static_instance"></span><span id="WMI.GLOSS_STATIC_INSTANCE"></span>**istanza statica**
</dt> <dd>

Un'istanza di una classe CIM che viene archiviata in modo permanente nel [*repository CIM*](gloss-c.md) e rimane valida fino a quando non viene eliminata in modo esplicito, neanche tra i riavvii del sistema.

</dd> <dt>

<span id="wmi.gloss_static_method"></span><span id="WMI.GLOSS_STATIC_METHOD"></span>**Metodo statico**
</dt> <dd>

Metodo definito in una classe CIM eseguita recuperando la definizione della classe anziché recuperare un'istanza della classe.

</dd> <dt>

<span id="wmi.gloss_subschema"></span><span id="WMI.GLOSS_SUBSCHEMA"></span>**sottoschema**
</dt> <dd>

Parte di uno *schema* di proprietà di un'organizzazione specifica. [*Win32schema*](gloss-w.md) è un esempio di un sottoschema.

</dd> <dt>

<span id="wmi.gloss_system_class"></span><span id="WMI.GLOSS_SYSTEM_CLASS"></span>**classe di sistema**
</dt> <dd>

Classe definita dall' [*CIM Object Manager*](gloss-c.md) per supportare le funzionalità principali, ad esempio la notifica degli eventi, la sicurezza e la localizzazione. Una classe di sistema viene definita automaticamente in ogni [*spazio dei nomi*](gloss-n.md). Una classe di sistema deriva dalla classe di base astratta [**\_ \_ SystemClass**](--systemclass.md).

</dd> <dt>

<span id="wmi.gloss_system_monitor"></span><span id="WMI.GLOSS_SYSTEM_MONITOR"></span>**Monitoraggio di sistema**
</dt> <dd>

Un'utilità (CIM) che rappresenta l'interfaccia utente grafica per il monitoraggio delle prestazioni.

</dd> <dt>

<span id="wmi.gloss_system_property"></span><span id="WMI.GLOSS_SYSTEM_PROPERTY"></span>**Proprietà di sistema**
</dt> <dd>

Proprietà definita dall' [*CIM Object Manager*](gloss-c.md) per fornire informazioni applicabili a ogni classe, ad esempio nome, derivazione e [*spazio dei nomi*](gloss-n.md).

</dd> </dl>

 

 



