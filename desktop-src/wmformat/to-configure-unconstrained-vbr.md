---
title: Per configurare vbr senza vincoli
description: Per configurare vbr senza vincoli
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- flussi, configurazione di flussi VBR
- flussi,velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, configurazione di VBR senza vincoli
- velocità in bit variabile (VBR), configurazione senza vincoli
- VBR (velocità in bit variabile), configurazione senza vincoli
- profili, configurazione di vbr senza vincoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff73a0aac8d13f015175080aac6eb580fc9686c67d892b14e4714746c8cea34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807761"
---
# <a name="to-configure-unconstrained-vbr"></a>Per configurare vbr senza vincoli

È possibile usare la codifica VBR (Variable Bit Rate) senza vincoli in un flusso per specificare una velocità in bit media che verrà mantenuta nel contenuto codificato. VbR non vincolato differisce dal normale CBR in modo che la varianza in bit rate in tutto il flusso può essere maggiore.

La velocità in bit del flusso, impostata con [**IWMStreamConfig::SetBitrate,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)viene usata come velocità in bit media desiderata. Al termine della codifica del flusso, è possibile usare [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) per recuperare due proprietà aggiuntive: **g \_ wszVBRPeak** e **g \_ wszBufferAverage**. Queste proprietà descrivono rispettivamente la velocità in bit di picco del contenuto codificato e la finestra media del buffer del contenuto.

VbR senza vincoli deve essere usato insieme alla codifica a due passi. La codifica a due passi non è impostata nel profilo. È necessario configurare il writer per eseguire un passaggio di pre-elaborazione prima di scrivere il flusso. Per altre informazioni sull'uso della codifica a due passi, vedere [Using Two-Pass Encoding](using-two-pass-encoding.md).

Per configurare un flusso in un profilo da codificare con VBR senza vincoli, seguire questa procedura:

1.  Creare un oggetto di gestione profili chiamando la [**funzione WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
2.  Aprire un profilo esistente a cui si vuole aggiungere il supporto vbr. Per altre informazioni sull'apertura dei profili, vedere [Uso dei profili](working-with-profiles.md).
3.  Ottenere un oggetto di configurazione del flusso per il flusso da usare chiamando [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Ottenere un puntatore [**all'interfaccia IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig::QueryInterface**.
5.  Abilitare la codifica VBR per il flusso chiamando [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per la **proprietà g \_ wszVBREnabled.**
6.  Impostare **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** su zero con **IWMPropertyVault::SetProperty**.
7.  Salvare le modifiche apportate al flusso chiamando [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Salvare il profilo o passarlo all'oggetto writer.
9.  Configurare il writer per eseguire un passaggio di pre-elaborazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di VBR Flussi**](configuring-vbr-streams.md)
</dt> </dl>

 

 




