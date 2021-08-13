---
description: Definisce il tipo di endpoint che è possibile usare per connettersi a un servizio.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumerazione UpdateEndpointType (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 7fbfd67b3009fbe904284ea7a92cdea996d0a6e23a43a17639eb567d66536917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462911"
---
# <a name="updateendpointtype-enumeration"></a>Enumerazione UpdateEndpointType

Definisce il tipo di endpoint che è possibile usare per connettersi a un servizio.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**
</dt> <dd>

Endpoint client-server utilizzato per connettersi al servizio di aggiornamento, ad esempio Windows Update, Microsoft Update e server WSUS in un ambiente aziendale, per trovare informazioni sugli aggiornamenti che possono essere applicabili al computer.

Il servizio di aggiornamento restituisce informazioni sugli aggiornamenti pubblicati, aggiornati o ritirati dall'ultima volta in cui il client ha eseguito una sincronizzazione con il server.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**UetReporting**
</dt> <dd>

Endpoint di report utilizzato quando il client segnala i risultati di analisi, download e installazioni nel servizio di aggiornamento.

Nel caso di servizi pubblici (Windows update e Microsoft Update), questa operazione viene eseguita a scopo di monitoraggio della qualità.

Nel caso di servizi privati, ad esempio un server WSUS aziendale, questo tipo di endpoint consente anche al server di raccogliere l'inventario e altre informazioni sui computer client in gestione.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**
</dt> <dd>

Endpoint di aggiornamento automatico utilizzato quando il computer client contatta un servizio di aggiornamento per verificare se è disponibile una nuova versione del software client Windows Update Agent.

L'endpoint di aggiornamento automatico usa un protocollo diverso e quindi l'endpoint Client-Server in modo che gli aggiornamenti automatici possano essere distribuiti anche se è presente una condizione di errore che potrebbe impedire alla normale sincronizzazione client-server di funzionare in un computer client specifico.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**
</dt> <dd>

Endpoint del regolamento utilizzato quando il computer client contatta il servizio di regolamento per eseguire un determinato aggiornamento applicabile al computer di destinazione.

Il servizio di regolamento può indicare se l'aggiornamento è "regolamentato" (noto anche come "limitato"). In altre parole, il servizio di regolamento può indicare al computer client che non deve agire su un determinato aggiornamento, anche se sembra applicabile.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**UetSimpleTargeting**
</dt> <dd>

Endpoint con destinazione semplice usato solo con servizi privati (server WSUS in ambienti aziendali). In un ambiente aziendale, i computer client possono essere assegnati a gruppi di destinazione specifici e gli aggiornamenti possono essere approvati per l'installazione in computer in alcuni gruppi ma non in altri.

Ad esempio, l'amministratore di WSUS può creare un gruppo "Test" per i computer usati per testare nuovi aggiornamenti e l'amministratore può approvare gli aggiornamenti rilasciati di recente per l'installazione nei computer del gruppo Test senza approvarli per l'installazione in altri computer dell'organizzazione. Lo scambio di destinazione semplice viene usato per consentire a un computer client di registrarsi con il server WSUS e per consentire al server di indicare al computer client il gruppo in cui si trova.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**
</dt> <dd>

Endpoint client-server protetto che consente a un client di ottenere informazioni sulle app che necessitano di licenze per poter essere usate in un computer client. Questo framework di gestione delle licenze viene attualmente usato Windows 8 per distribuire le app e gli aggiornamenti ottenuti tramite Windows Store. L'endpoint client-server protetto non viene attualmente usato da Windows Update, Microsoft Update o WSUS.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**
</dt> <dd>

L'endpoint secondary-service-authentication viene usato da un client per fornire l'autenticazione prima di ottenere informazioni sulle app che necessitano di licenze in modo che possano essere usate in un computer client. Questo framework di gestione delle licenze viene attualmente utilizzato solo Windows 8 distribuire app e aggiornamenti ottenuti tramite Windows Store. L'endpoint di autenticazione del servizio secondario non è attualmente usato Windows Update, Microsoft Update o WSUS.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |



 

 




