---
title: Recupero delle informazioni sul profilo durante la riproduzione
description: Recupero delle informazioni sul profilo durante la riproduzione
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK, profili
- ASF (Advanced Systems Format), profili
- ASF (formato avanzato dei sistemi), profili
- Formato di sistemi avanzati (ASF), esclusione reciproca
- ASF (formato avanzato dei sistemi), esclusione reciproca
- ASF (Advanced Systems Format), condivisione della larghezza di banda
- ASF (formato avanzato dei sistemi), condivisione della larghezza di banda
- flussi, recupero di informazioni sul profilo durante la riproduzione
- profili, recupero di informazioni durante la riproduzione
- esclusione reciproca, recupero di informazioni sul profilo durante la riproduzione
- condivisione della larghezza di banda, recupero delle informazioni sul profilo durante la riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117387"
---
# <a name="getting-profile-information-at-playback"></a>Recupero delle informazioni sul profilo durante la riproduzione

Le informazioni del profilo utilizzato per creare un file vengono archiviate nella sezione dell'intestazione del file. Entrambi gli oggetti Reader possono accedere alle informazioni sul profilo dall'intestazione del file. Esistono diversi motivi per cui è possibile che si desideri accedere ai dati del profilo dal reader. In genere, è necessario recuperare informazioni sui flussi, sugli oggetti di esclusione reciproca e sugli oggetti di condivisione della larghezza di banda.

È possibile eseguire query sull'oggetto Reader asincrono e sull'oggetto Reader sincrono per l'interfaccia [**IWMProfile**](iwmprofile.md) . Nessuna modifica apportata alle informazioni sul profilo può avere alcun effetto sul file nel lettore. Per ulteriori informazioni sull'accesso alle informazioni sul profilo, vedere [utilizzo dei profili](working-with-profiles.md).

## <a name="stream-information"></a>Informazioni sul flusso

A volte è importante capire come viene configurato un flusso. Quando si recuperano le proprietà dei supporti da uno degli oggetti Reader, si ottengono le proprietà degli output. Le proprietà di output descrivono il modo in cui i dati non compressi da un flusso verranno recapitati dal lettore, non come il flusso viene configurato nel file ASF.

Quando si ricevono esempi di flusso non compressi da uno dei due oggetti Reader, è necessario usare le informazioni sul profilo per identificare il formato dei dati compressi. Questa operazione è particolarmente importante se si intende scrivere il flusso compresso in un altro file ASF.

È anche necessario accedere alle informazioni sul flusso quando si usa la ricompressione intelligente per transcodificare un flusso audio a una velocità in bit più bassa.

Potrebbe essere necessario determinare se un flusso è stato scritto utilizzando la codifica con velocità in bit variabile (VBR). Non è possibile accedere alle informazioni di VBR dall'interfaccia **IWMProfile** di uno dei due oggetti Reader. Ciò è dovuto al fatto che le informazioni VBR non vengono archiviate nel file dopo la codifica. È possibile determinare se un flusso è stato creato usando la codifica VBR ottenendo un puntatore all'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) dell'oggetto Reader e chiamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname). È necessario specificare il numero del flusso e passare g \_ wszIsVBR come nome dell'attributo.

## <a name="mutual-exclusion-information"></a>Informazioni sull'esclusione reciproca

Se si desidera creare un'applicazione di lettura che utilizza l'esclusione reciproca, sarà necessario accedere alle informazioni sugli oggetti di esclusione reciproca inclusi nel profilo. Per tutti i tipi di esclusione reciproca ad eccezione della velocità in bit, l'applicazione di lettura è responsabile di qualsiasi cambio di flusso necessario. Per cambiare flusso, è necessario individuare i flussi.

## <a name="bandwidth-sharing-information"></a>Informazioni sulla condivisione della larghezza di banda

Gli oggetti di condivisione della larghezza di banda inclusi in un profilo sono inclusi solo a scopo informativo. Né l'oggetto writer né uno degli oggetti Reader esegue alcuna azione a causa dei dati di condivisione della larghezza di banda. Se si vuole usare la condivisione della larghezza di banda nell'applicazione di lettura, è necessario accedere alle informazioni di condivisione della larghezza di banda dai dati del profilo.

> [!Note]  
> Non tutte le informazioni del profilo utilizzato per creare un file sono presenti nell'intestazione del file. Come regola generale, i dati utilizzati solo al momento della codifica non vengono mantenuti nel file. Sono incluse le impostazioni di input impostate tramite il metodo [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) e le proprietà impostate utilizzando il metodo [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




