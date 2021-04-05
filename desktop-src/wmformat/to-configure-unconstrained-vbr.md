---
title: Per configurare il VBR non vincolato
description: Per configurare il VBR non vincolato
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- flussi, configurazione di flussi VBR
- flussi, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, configurazione di VBR non vincolato
- velocità in bit variabile (VBR), configurazione non vincolata
- VBR (velocità in bit variabile), configurazione non vincolata
- profili, configurazione di VBR non vincolato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117450"
---
# <a name="to-configure-unconstrained-vbr"></a>Per configurare il VBR non vincolato

È possibile utilizzare la codifica della velocità in bit variabile (VBR) non vincolata in un flusso per specificare una velocità in bit media che verrà mantenuta nel contenuto codificato. Il VBR non vincolato è diverso da quello normale in quanto la varianza nella velocità in bit nel flusso può essere maggiore.

La velocità in bit del flusso, impostata con [**IWMStreamConfig:: bitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), viene utilizzata come velocità in bit media desiderata. Quando la codifica del flusso è completa, è possibile usare [**IWMPropertyVault:: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) per recuperare due proprietà aggiuntive: **g \_ wszVBRPeak** e **g \_ wszBufferAverage**. Queste proprietà descrivono rispettivamente la velocità in bit massima del contenuto codificato e la finestra media del buffer del contenuto.

È necessario usare il VBR non vincolato insieme alla codifica a due passaggi. La codifica a due passaggi non è impostata nel profilo. È necessario configurare il writer per eseguire un passaggio di pre-elaborazione prima di scrivere il flusso. Per ulteriori informazioni sull'utilizzo della codifica a due passaggi, vedere [utilizzo della codifica Two-Pass](using-two-pass-encoding.md).

Per configurare un flusso in un profilo da codificare con VBR non vincolato, seguire questa procedura:

1.  Creare un oggetto di gestione del profilo chiamando la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Aprire un profilo esistente a cui si desidera aggiungere il supporto per VBR. Per ulteriori informazioni sull'apertura di profili, vedere [utilizzo dei profili](working-with-profiles.md).
3.  Ottenere un oggetto di configurazione del flusso per il flusso che si vuole usare chiamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Ottenere un puntatore all'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.
5.  Abilitare la codifica VBR per il flusso chiamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per la proprietà **g \_ wszVBREnabled** .
6.  Impostare **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** su zero con **IWMPropertyVault:: SetProperty**.
7.  Salvare le modifiche apportate al flusso chiamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Salvare il profilo o passarlo all'oggetto writer.
9.  Configurare il writer per eseguire un passaggio di pre-elaborazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




