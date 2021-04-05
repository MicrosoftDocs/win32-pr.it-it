---
title: Per configurare il VBR vincolato
description: Per configurare il VBR vincolato
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- flussi, configurazione di flussi VBR
- flussi, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, configurazione di VBR vincolato
- velocità in bit variabile (VBR), configurazione vincolata
- VBR (velocità in bit variabile), configurazione vincolata
- profili, configurazione di VBR vincolato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046432"
---
# <a name="to-configure-constrained-vbr"></a>Per configurare il VBR vincolato

È possibile usare la codifica con velocità in bit variabile (VBR) vincolata in un flusso per specificare una velocità in bit media che verrà mantenuta nel contenuto codificato. È inoltre possibile specificare la velocità massima in bit del flusso e la finestra massima del buffer richiesta.

Non è possibile conoscere la velocità in bit media per un flusso VBR vincolato prima della codifica, ma è possibile usare una stima approssimativa. Come regola generale, la velocità in bit massima specificata finirà da due a tre volte la velocità media in bit.

È necessario usare il VBR vincolato insieme alla codifica a due passaggi. La codifica a due passaggi non è impostata nel profilo. È necessario configurare il writer per eseguire un passaggio di pre-elaborazione prima di scrivere il flusso. Per ulteriori informazioni sull'utilizzo della codifica a due passaggi, vedere [utilizzo della codifica Two-Pass](using-two-pass-encoding.md).

Per configurare un flusso in un profilo per l'uso della codifica VBR vincolata, seguire questa procedura.

1.  Creare un oggetto di gestione del profilo chiamando la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Aprire un profilo esistente a cui si desidera aggiungere il supporto per VBR. Per ulteriori informazioni sull'apertura di profili, vedere [utilizzo dei profili](working-with-profiles.md).
3.  Ottenere un oggetto di configurazione del flusso per il flusso che si vuole usare chiamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Ottenere un puntatore all'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.
5.  Abilitare la codifica VBR per il flusso chiamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per la proprietà **g \_ wszVBREnabled** .
6.  Usare le chiamate a **IWMPropertyVault:: SetProperty** per impostare i valori massimi desiderati per le proprietà **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** .
7.  Salvare le modifiche apportate al flusso chiamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Salvare il profilo o passarlo all'oggetto writer.
9.  Configurare il writer per eseguire un passaggio di pre-elaborazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




