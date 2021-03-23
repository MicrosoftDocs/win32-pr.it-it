---
title: Uso del livello di debug DirectML
description: Il livello di debug DirectML è un componente della fase di sviluppo facoltativo che consente di eseguire il debug del codice DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548829"
---
# <a name="using-the-directml-debug-layer"></a>Uso del livello di debug DirectML

Il livello di debug DirectML è un componente della fase di sviluppo facoltativo che consente di eseguire il debug del codice DirectML. Il livello di debug fa parte di un pacchetto di strumenti di grafica separato, distribuito come [funzionalità su richiesta](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (Dom). Per usare il livello di debug, è necessario che nel sistema siano installati gli strumenti di grafica Dom.

Si consiglia di abilitare il livello di debug durante lo sviluppo di applicazioni tramite DirectML, perché può fornire informazioni inestimabili in caso di utilizzo non valido dell'API.

## <a name="installing-the-directml-debug-layer"></a>Installazione del livello di debug DirectML

Per installare il pacchetto di funzionalità-on-demand (Dom) degli strumenti di grafica facoltativi, eseguire il comando seguente da un prompt di PowerShell per amministratore.

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

In alternativa, è possibile installare il pacchetto strumenti di grafica dalle impostazioni di Windows 10. Passare a **Impostazioni**  >  **app app**  >  **& funzionalità**  >  **opzionali**  >  **aggiungere una funzionalità** > quindi selezionare **strumenti di grafica**.

## <a name="enabling-the-directml-debug-layer"></a>Abilitazione del livello di debug DirectML

Una volta installato il pacchetto di strumenti di grafica, è possibile abilitare il livello di debug DirectML fornendo  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) quando si chiama [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).

> [!IMPORTANT]
> Per prima cosa, è necessario abilitare il livello di debug Direct3D 12. *Quindi* abilitare il livello di debug DirectML chiamando **DMLCreateDevice**.

Dopo aver abilitato il livello di debug DirectML, gli eventuali errori DirectML o chiamate API non valide comporteranno la creazione di informazioni di debug come output di debug. Ecco un esempio.

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a>Vedi anche

* [DMLCreateDevice (funzione)](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [Funzionalità disponibili su richiesta](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [Usare la convalida basata su GPU con il livello di debug Direct3D 12](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [Riferimento al livello di debug Direct3D 12](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
