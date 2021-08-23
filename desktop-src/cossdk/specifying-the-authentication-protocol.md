---
description: Specifica del protocollo di autenticazione
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Specifica del protocollo di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c4688894543a45f49c4af470658da97e30a159c47025398ac7c7ae5e0620e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610511"
---
# <a name="specifying-the-authentication-protocol"></a>Specifica del protocollo di autenticazione

A seconda dei requisiti di sicurezza del sito, è possibile richiedere al servizio dei componenti in coda di verificare sempre l'identità di un client, di non verificare mai l'identità di un client o di verificare l'identità di un client solo se il componente è configurato per richiedere l'autenticazione anche quando non vi si accede tramite una coda.

> [!Note]  
> Per usare un componente in coda in modalità gruppo di lavoro, il livello di autenticazione deve essere impostato su nessuno.

 

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per specificare il protocollo di autenticazione, seguire questa procedura:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in Servizi componenti **aprire** la cartella **Applicazioni COM+** associata al computer da gestire.

2.  Fare clic con il pulsante destro del mouse sull'applicazione in coda per la quale si desidera specificare il protocollo di autenticazione, quindi **scegliere Proprietà**.

3.  Selezionare la **scheda Accodamento** nella finestra di dialogo delle proprietà.

4.  In **Autenticazione messaggi MSMQ** selezionare il pulsante di opzione associato al protocollo di autenticazione che si vuole implementare.

5.  Fare clic su **OK**.

## <a name="visual-basic"></a>Visual Basic

Usare il *parametro AuthLevel* quando si attiva l'applicazione in coda come descritto in [Uso del moniker coda](using-the-queue-moniker.md).

## <a name="cc"></a>C/C++

Usare il *parametro AuthLevel* quando si attiva l'applicazione in coda come descritto in [Uso del moniker coda](using-the-queue-moniker.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza dei componenti in coda](queued-components-security.md)
</dt> <dt>

[Limitazioni di sicurezza in modalità gruppo di lavoro](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



