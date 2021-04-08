---
title: Per utilizzare profili con il writer
description: Per utilizzare profili con il writer
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK, scrittura di file ASF
- Windows Media Format SDK, creazione di file ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Formato di sistemi avanzati (ASF), scrittura di file
- ASF (Advanced Systems Format), scrittura di file
- ASF (Advanced Systems Format), creazione di file
- ASF (Advanced Systems Format), creazione di file
- profili, creazione di file ASF
- profili, scrittura di file ASF
- profili, creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046429"
---
# <a name="to-use-profiles-with-the-writer"></a>Per utilizzare profili con il writer

Il writer usa i dati di profilo per creare file ASF. È necessario specificare un profilo da usare prima di eseguire altre operazioni con il writer.

È possibile impostare un profilo di sistema da usare con il writer passando l'ID del profilo al metodo [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .

Per specificare un profilo personalizzato da usare con il writer, è necessario ottenere un'interfaccia [**IWMProfile**](iwmprofile.md) per un oggetto contenente i dati del profilo desiderato. Per eseguire questa operazione, è possibile utilizzare uno dei metodi di caricamento dell'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Quando si dispone di un'interfaccia **IWMProfile** valida, è possibile passare un puntatore al metodo [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) . Per ulteriori informazioni sulle impostazioni del profilo, vedere [utilizzo dei profili](working-with-profiles.md).

Se si apportano modifiche all'oggetto profilo utilizzando l'interfaccia **IWMProfile** dopo aver impostato il profilo nel writer, è **necessario chiamare di nuovo il profilo,** altrimenti le modifiche non verranno riflesse nel writer. Tuttavia, la chiamata a **seprofile** Reimposta tutti gli attributi di intestazione, pertanto assicurarsi di impostare gli attributi di intestazione obbligatori dopo la chiamata a questo metodo.

La funzione di esempio seguente imposta il profilo su "Windows Media Video 8 per i modem di connessione remota (56 Kbps)":


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> Non esistono profili di sistema predefiniti che usano i codec della serie Windows Media Audio e video 9. Per ulteriori informazioni, vedere [riutilizzo delle configurazioni di flusso](reusing-stream-configurations.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




