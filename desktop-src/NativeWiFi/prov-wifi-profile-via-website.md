---
title: Effettuare il provisioning di un profilo Wi-Fi tramite un sito Web
description: Consente agli utenti di scaricare un profilo da un sito Web ed eseguirne il provisioning.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963430"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a>Effettuare il provisioning di un profilo Wi-Fi tramite un sito Web

Il flusso di lavoro descritto in questo argomento è stato introdotto in Windows 10, versione 2004. In questo argomento viene illustrato come configurare un sito Web in modo che un utente possa eseguire il provisioning di un profilo per una rete Passpoint (o per una rete normale) prima di trasferirsi nell'intervallo dei corrispondenti punti di accesso Wi-Fi. Uno scenario di esempio è quello di un utente che può pianificare di visitare un aeroporto o una conferenza per la prima volta e vuole prepararsi in anticipo scaricando ed effettuando il provisioning di un profilo a casa.

Gli sviluppatori abilitano il flusso di lavoro fornendo un profilo XML e configurando un sito Web. Gli utenti possono quindi effettuare il provisioning di un profilo di Wi-Fi eseguendone il download dal sito Web tramite un Web browser. Sul dispositivo dell'utente, viene eseguito il provisioning del profilo di Wi-Fi usando l'attivazione dell'URI e l'app **Impostazioni** di Windows.

Questo flusso di lavoro sostituisce il meccanismo in Internet Explorer per il provisioning di Wi-Fi profili che si basa su API JavaScript specifiche di Microsoft. Questo nuovo flusso di lavoro dovrebbe funzionare con tutti i browser principali.

## <a name="the-workflow-in-more-detail"></a>Il flusso di lavoro in modo più dettagliato

È possibile attivare questo flusso di lavoro da un collegamento ipertestuale che include come argomento l'URI di download del documento XML di provisioning.

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

Il markup HTML seguente, ad esempio, fornisce un collegamento per installare i profili trovati in un documento ipotetico `http://contoso.com/ProvisioningDoc.xml` .

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

Il codice XML deve essere conforme allo schema di provisioning (vedere [provisioning dell'account](/windows-hardware/drivers/mobilebroadband/account-provisioning)). Il codice XML deve includere anche uno o più elementi [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   .Ogni profilo verrà visualizzato nella finestra di dialogo **Aggiungi** descritta di seguito.

Quando l'utente fa clic sul collegamento HTML, il flusso di lavoro di installazione viene richiamato nell'app **Impostazioni** . Il documento XML di provisioning viene scaricato dall'app **Impostazioni** . Una volta scaricato, vengono visualizzate le informazioni sui profili, sulla firma e sul firmatario (purché il documento rispetti lo schema).

![App impostazioni](images/install-dialog.png)

Il pulsante **Aggiungi** nella finestra di dialogo nell'app **Impostazioni** è abilitato solo se il file di provisioning è firmato e attendibile.

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a>Nella pagina Web determinare se questo flusso di lavoro è supportato

In JavaScript non esiste alcun modo per determinare la versione di build esatta di Windows. Tuttavia, se l'utente usa il Web browser Microsoft Edge, è possibile determinare la versione di Edge controllando il valore dell' `User-agent` intestazione HTTP. Se la versione è maggiore o uguale a `18.nnnnn` , il flusso di lavoro è supportato.

## <a name="related-topics"></a>Argomenti correlati

* [Provisioning dell'account](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [Elemento WLANProfile](./wlan-profileschema-wlanprofile-element.md)