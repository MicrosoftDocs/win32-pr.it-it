---
title: Per configurare Quality-Based VBR
description: Per configurare Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- flussi, configurazione di flussi VBR
- flussi,velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, configurazione di vbr basato sulla qualità
- velocità in bit variabile (VBR), configurazione basata sulla qualità
- VBR (velocità in bit variabile), configurazione basata sulla qualità
- profili, configurazione di vbr basato sulla qualità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b1181d722909478b29e1ffbe5f5b53cb919d80e3922e055eecdf34c334a382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845636"
---
# <a name="to-configure-quality-based-vbr"></a>Per configurare Quality-Based VBR

È possibile usare la codifica VBR (Quality-Based Variable Bit Rate) in un flusso per specificare un livello di qualità che verrà mantenuto per l'intero flusso, indipendentemente dal numero di bit che ne derivano.

Per i flussi video VBR basati sulla qualità, è necessario specificare un livello di qualità da 1 a 100, con 100 che rappresenta la qualità più elevata. Attualmente sono disponibili solo 30 impostazioni di qualità discrete. I livelli di qualità seguenti equidodono alle impostazioni di qualità discrete: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100. I numeri compresi tra due valori consecutivi nell'elenco precedente equidominano alla stessa impostazione di qualità del numero inferiore. Ad esempio, sono elencati 1 e 4, quindi 2 e 3 hanno entrambi la stessa impostazione di qualità 1.

Per i flussi audio, è possibile enumerare le modalità disponibili e recuperare un oggetto di configurazione del flusso. Per altre informazioni, vedere [Per enumerare i formati di codec.](to-enumerate-codec-formats.md)

Quando si usa un video VBR basato sulla qualità, è necessario impostare il membro **dwBitrate** della struttura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) su un valore positivo. Questo valore non viene usato dal writer, ma il passaggio di zero o un numero negativo può causare errori durante la scrittura.

Per configurare un flusso in un profilo da codificare con vbr basato sulla qualità, seguire questa procedura.

1.  Creare un oggetto di gestione del profilo chiamando la [**funzione WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
2.  Aprire un profilo esistente a cui si vuole aggiungere il supporto vbr. Per altre informazioni sull'apertura dei profili, vedere [Uso dei profili](working-with-profiles.md).
3.  Ottenere un oggetto di configurazione del flusso per il flusso da usare chiamando [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Ottenere un puntatore [**all'interfaccia IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig::QueryInterface**.
5.  Abilitare VBR per il flusso chiamando [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per la **proprietà g \_ wszVBREnabled.**
6.  Impostare il livello di qualità per il flusso VBR chiamando **IWMPropertyVault::SetProperty** per la proprietà **\_ g wszVBRQuality.**
7.  Impostare **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** su zero con **IWMPropertyVault::SetProperty**.
8.  Salvare le modifiche apportate al flusso chiamando [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
9.  Salvare il profilo o passarlo all'oggetto writer e iniziare a scrivere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di VBR Flussi**](configuring-vbr-streams.md)
</dt> </dl>

 

 




