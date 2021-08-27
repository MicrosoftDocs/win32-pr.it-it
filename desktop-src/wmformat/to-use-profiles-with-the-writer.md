---
title: Per utilizzare profili con il writer
description: Per utilizzare profili con il writer
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK, scrittura di file ASF
- Windows Media Format SDK, creazione di file ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), scrittura di file
- ASF (Advanced Systems Format), scrittura di file
- Advanced Systems Format (ASF), creazione di file
- ASF (Advanced Systems Format), creazione di file
- profili, creazione di file ASF
- profili, scrittura di file ASF
- profili, creazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0184469215dd109bcc4ca120e2db9cbead8b9bd250cb017456f9d7d08ea46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027269"
---
# <a name="to-use-profiles-with-the-writer"></a>Per utilizzare profili con il writer

Il writer usa i dati del profilo per creare file ASF. È necessario specificare un profilo da usare prima di eseguire qualsiasi altra operazione con il writer.

È possibile impostare un profilo di sistema da usare con il writer passando l'ID del profilo al [**metodo IWMWriter::SetProfileByID.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)

Per specificare un profilo personalizzato da usare con il writer, è necessario ottenere [**un'interfaccia IWMProfile**](iwmprofile.md) per un oggetto contenente i dati del profilo desiderati. A tale scopo, è possibile usare uno dei metodi di caricamento [**dell'interfaccia IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) Dopo aver creato **un'interfaccia IWMProfile** valida, è possibile passarvi un puntatore al [**metodo IWMWriter::SetProfile.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) Per altre informazioni sulle impostazioni del profilo, vedere [Utilizzo dei profili.](working-with-profiles.md)

Se si apportano modifiche all'oggetto profilo usando l'interfaccia **IWMProfile** dopo aver impostato il profilo nel writer, è necessario chiamare di nuovo **SetProfile.** In caso contrario, le modifiche non verranno riflesse nel writer. Tuttavia, la chiamata **a SetProfile** reimposta tutti gli attributi di intestazione, quindi assicurarsi di impostare gli attributi di intestazione necessari dopo aver chiamato questo metodo.

La funzione di esempio seguente imposta il profilo su "Windows Media Video 8 for Dial-up Modems (56 Kbps)":


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
> Non sono disponibili profili di sistema predefiniti che usano Windows codec Media Audio e Video 9 Series. Per altre informazioni, vedere [Riutilizzo delle configurazioni di flusso.](reusing-stream-configurations.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




