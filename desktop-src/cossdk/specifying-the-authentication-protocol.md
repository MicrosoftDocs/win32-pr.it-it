---
description: Specifica del protocollo di autenticazione
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Specifica del protocollo di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483421"
---
# <a name="specifying-the-authentication-protocol"></a>Specifica del protocollo di autenticazione

A seconda dei requisiti di sicurezza nel sito, è possibile richiedere che il servizio componenti in coda verifichi sempre l'identità di un client, non per verificare mai l'identità di un client o per verificare l'identità di un client solo se il componente è configurato per richiedere l'autenticazione anche quando non è possibile accedervi tramite una coda.

> [!Note]  
> Per utilizzare un componente in coda in modalità gruppo di lavoro, il livello di autenticazione deve essere impostato su nessuno.

 

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per specificare il protocollo di autenticazione, attenersi alla procedura seguente:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.

2.  Fare clic con il pulsante destro del mouse sull'applicazione in coda per la quale si desidera specificare il protocollo di autenticazione, quindi scegliere **Proprietà**.

3.  Selezionare la scheda **Accodamento** nella finestra di dialogo Proprietà.

4.  In **autenticazione messaggi MSMQ** selezionare il pulsante di opzione associato al protocollo di autenticazione che si desidera implementare.

5.  Fare clic su **OK**.

## <a name="visual-basic"></a>Visual Basic

Usare il parametro *AUTHLEVEL* quando si attiva l'applicazione in coda come descritto in [uso del moniker della coda](using-the-queue-moniker.md).

## <a name="cc"></a>C/C++

Usare il parametro *AUTHLEVEL* quando si attiva l'applicazione in coda come descritto in [uso del moniker della coda](using-the-queue-moniker.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza dei componenti in coda](queued-components-security.md)
</dt> <dt>

[Limitazioni di sicurezza in modalità gruppo di lavoro](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



