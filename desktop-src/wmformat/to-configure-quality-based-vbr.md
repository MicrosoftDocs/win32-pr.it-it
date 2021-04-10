---
title: Per configurare Quality-Based VBR
description: Per configurare Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- flussi, configurazione di flussi VBR
- flussi, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, configurazione di VBR basato sulla qualità
- velocità in bit variabile (VBR), configurazione basata sulla qualità
- VBR (velocità in bit variabile), configurazione basata sulla qualità
- profili, configurazione di VBR basato sulla qualità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103956262"
---
# <a name="to-configure-quality-based-vbr"></a>Per configurare Quality-Based VBR

È possibile usare la codifica di velocità in bit variabile (VBR) basata sulla qualità in un flusso per specificare un livello di qualità che verrà mantenuto per l'intero flusso, indipendentemente dai requisiti di velocità in bit che risultano.

Per i flussi video VBR basati sulla qualità, è necessario specificare un livello di qualità compreso tra 1 e 100, con 100 che rappresentano la qualità più elevata. Al momento sono disponibili solo 30 impostazioni di qualità discrete. I livelli di qualità seguenti equivalgono a impostazioni di qualità discrete: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100. I numeri tra due valori consecutivi nell'elenco precedente corrispondono alla stessa impostazione di qualità del numero inferiore. Ad esempio, 1 e 4 sono elencati, quindi 2 e 3 generano entrambe la stessa impostazione di qualità di 1.

Per i flussi audio, è possibile enumerare le modalità disponibili e recuperare un oggetto di configurazione del flusso. Per ulteriori informazioni, vedere [per enumerare i formati di codec](to-enumerate-codec-formats.md).

Quando si usa il video VBR basato sulla qualità, è necessario impostare il membro **dwBitrate** della struttura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) su un valore positivo. Questo valore non viene utilizzato dal writer, ma il passaggio a zero o a un numero negativo può causare errori durante la scrittura.

Per configurare un flusso in un profilo da codificare con VBR basato sulla qualità, seguire questa procedura.

1.  Creare un oggetto di gestione del profilo chiamando la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Aprire un profilo esistente a cui si desidera aggiungere il supporto per VBR. Per ulteriori informazioni sull'apertura di profili, vedere [utilizzo dei profili](working-with-profiles.md).
3.  Ottenere un oggetto di configurazione del flusso per il flusso che si vuole usare chiamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Ottenere un puntatore all'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.
5.  Abilitare VBR per il flusso chiamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per la proprietà **g \_ wszVBREnabled** .
6.  Impostare il livello di qualità per il flusso VBR chiamando **IWMPropertyVault:: SetProperty** per la proprietà **g \_ wszVBRQuality** .
7.  Impostare **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** su zero con **IWMPropertyVault:: SetProperty**.
8.  Salvare le modifiche apportate al flusso chiamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
9.  Salvare il profilo o passarlo all'oggetto writer e iniziare a scrivere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




