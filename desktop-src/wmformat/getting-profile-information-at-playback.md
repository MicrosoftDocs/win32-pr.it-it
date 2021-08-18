---
title: Recupero delle informazioni del profilo durante la riproduzione
description: Recupero delle informazioni del profilo durante la riproduzione
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK, profili
- Advanced Systems Format (ASF), profiles
- ASF (Advanced Systems Format),profiles
- Advanced Systems Format (ASF), esclusione reciproca
- ASF (Advanced Systems Format), esclusione reciproca
- Advanced Systems Format (ASF), bandwidth sharing
- ASF (Advanced Systems Format), condivisione della larghezza di banda
- flussi, recupero di informazioni sul profilo durante la riproduzione
- profili,recupero di informazioni durante la riproduzione
- esclusione reciproca, recupero di informazioni sul profilo durante la riproduzione
- condivisione della larghezza di banda, recupero delle informazioni del profilo durante la riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0f9386301b426adb3c4c425ac9329309c7e45146e312cc41df0bd1c453d485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839921"
---
# <a name="getting-profile-information-at-playback"></a>Recupero delle informazioni del profilo durante la riproduzione

Le informazioni del profilo usato per creare un file vengono archiviate nella sezione di intestazione del file. Entrambi gli oggetti lettore possono accedere alle informazioni del profilo dall'intestazione del file. Esistono diversi motivi per cui potrebbe essere necessario accedere ai dati del profilo dal lettore. In genere, è necessario recuperare informazioni su flussi, oggetti di esclusione reciproca e oggetti di condivisione della larghezza di banda.

È possibile eseguire query sia sull'oggetto lettore asincrono che sull'oggetto lettore sincrono per [**l'interfaccia IWMProfile.**](iwmprofile.md) Nessuna modifica apportata alle informazioni del profilo può influire sul file nel lettore. Per altre informazioni sull'accesso alle informazioni sui profili, vedere [Uso dei profili](working-with-profiles.md).

## <a name="stream-information"></a>Informazioni sul flusso

A volte è importante sapere come viene configurato un flusso. Quando si recuperano le proprietà dei supporti da uno degli oggetti lettore, si ottengono le proprietà degli output. Le proprietà di output descrivono il modo in cui i dati non compressi da un flusso verranno recapitati dal lettore, non come il flusso viene configurato all'interno del file ASF.

Quando si ricevono esempi di flussi non compressi da uno degli oggetti lettore, è necessario usare le informazioni del profilo per identificare il formato dei dati compressi. Ciò è particolarmente importante se si scrive il flusso compresso in un altro file ASF.

È anche necessario accedere alle informazioni del flusso quando si usa la ricompressione intelligente per transcodificare un flusso audio a una velocità in bit inferiore.

È possibile determinare se un flusso è stato scritto usando la codifica VBR (Variable Bit Rate). Non è possibile accedere alle informazioni VBR **dall'interfaccia IWMProfile** di uno degli oggetti reader. Ciò è dovuto al fatto che le informazioni VBR non vengono archiviate nel file dopo la codifica. È possibile determinare se un flusso è stato creato usando la codifica VBR ottenendo un puntatore all'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) dell'oggetto reader e chiamando [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname). È necessario specificare il numero di flusso e passare g \_ wszIsVBR come nome dell'attributo.

## <a name="mutual-exclusion-information"></a>Informazioni sull'esclusione reciproca

Se si vuole creare un'applicazione di lettura che usa l'esclusione reciproca, è necessario accedere alle informazioni su eventuali oggetti di esclusione reciproca inclusi nel profilo. Per tutti i tipi di esclusione reciproca, ad eccezione della velocità in bit, l'applicazione di lettura è responsabile di qualsiasi cambio di flusso necessario. Per cambiare flusso, è necessario sapere quali sono i flussi.

## <a name="bandwidth-sharing-information"></a>Informazioni sulla condivisione della larghezza di banda

Gli oggetti di condivisione della larghezza di banda inclusi in un profilo sono inclusi solo a scopo informativo. Né l'oggetto writer né uno degli oggetti lettore prende alcuna azione a causa della condivisione dei dati della larghezza di banda. Se si vuole usare la condivisione della larghezza di banda nell'applicazione di lettura, è necessario accedere alle informazioni di condivisione della larghezza di banda dai dati del profilo.

> [!Note]  
> Non tutte le informazioni del profilo usato per creare un file sono presenti nell'intestazione del file. Come regola generale, i dati usati solo al momento della codifica non vengono resi persistenti nel file. Sono incluse le impostazioni di input impostate usando il metodo [**IWMWriterAdvanced2::SetInputSetting,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) nonché le proprietà impostate tramite il metodo [**IWMPropertyVault::SetProperty.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




