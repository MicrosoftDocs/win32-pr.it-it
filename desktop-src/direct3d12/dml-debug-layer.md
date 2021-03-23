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
# <a name="using-the-directml-debug-layer"></a><span data-ttu-id="05c1e-103">Uso del livello di debug DirectML</span><span class="sxs-lookup"><span data-stu-id="05c1e-103">Using the DirectML debug layer</span></span>

<span data-ttu-id="05c1e-104">Il livello di debug DirectML è un componente della fase di sviluppo facoltativo che consente di eseguire il debug del codice DirectML.</span><span class="sxs-lookup"><span data-stu-id="05c1e-104">The DirectML debug layer is an optional development-time component that helps you in debugging your DirectML code.</span></span> <span data-ttu-id="05c1e-105">Il livello di debug fa parte di un pacchetto di strumenti di grafica separato, distribuito come [funzionalità su richiesta](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (Dom).</span><span class="sxs-lookup"><span data-stu-id="05c1e-105">The debug layer is part of a separate Graphics Tools package, distributed as a [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD).</span></span> <span data-ttu-id="05c1e-106">Per usare il livello di debug, è necessario che nel sistema siano installati gli strumenti di grafica Dom.</span><span class="sxs-lookup"><span data-stu-id="05c1e-106">The Graphics Tools FOD must be installed on your system in order to use the debug layer.</span></span>

<span data-ttu-id="05c1e-107">Si consiglia di abilitare il livello di debug durante lo sviluppo di applicazioni tramite DirectML, perché può fornire informazioni inestimabili in caso di utilizzo non valido dell'API.</span><span class="sxs-lookup"><span data-stu-id="05c1e-107">We highly recommended that you enable the debug layer while developing applications using DirectML, because it can provide invaluable information in the event of invalid API usage.</span></span>

## <a name="installing-the-directml-debug-layer"></a><span data-ttu-id="05c1e-108">Installazione del livello di debug DirectML</span><span class="sxs-lookup"><span data-stu-id="05c1e-108">Installing the DirectML debug layer</span></span>

<span data-ttu-id="05c1e-109">Per installare il pacchetto di funzionalità-on-demand (Dom) degli strumenti di grafica facoltativi, eseguire il comando seguente da un prompt di PowerShell per amministratore.</span><span class="sxs-lookup"><span data-stu-id="05c1e-109">To install the optional Graphics Tools feature-on-demand (FOD) package, run the following command from an administrator Powershell prompt.</span></span>

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

<span data-ttu-id="05c1e-110">In alternativa, è possibile installare il pacchetto strumenti di grafica dalle impostazioni di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="05c1e-110">Alternatively, you can install the Graphics Tools package from within Windows 10 Settings.</span></span> <span data-ttu-id="05c1e-111">Passare a **Impostazioni**  >  **app app**  >  **& funzionalità**  >  **opzionali**  >  **aggiungere una funzionalità** > quindi selezionare **strumenti di grafica**.</span><span class="sxs-lookup"><span data-stu-id="05c1e-111">Navigate to **Settings** > **Apps** > **Apps & features** > **Optional features** > **Add a feature** > then select **Graphics Tools**.</span></span>

## <a name="enabling-the-directml-debug-layer"></a><span data-ttu-id="05c1e-112">Abilitazione del livello di debug DirectML</span><span class="sxs-lookup"><span data-stu-id="05c1e-112">Enabling the DirectML debug layer</span></span>

<span data-ttu-id="05c1e-113">Una volta installato il pacchetto di strumenti di grafica, è possibile abilitare il livello di debug DirectML fornendo  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) quando si chiama [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span><span class="sxs-lookup"><span data-stu-id="05c1e-113">Once the Graphics Tools package is installed, you can enable the DirectML debug layer by supplying  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) when you call [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05c1e-114">Per prima cosa, è necessario abilitare il livello di debug Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="05c1e-114">You must first enable the Direct3D 12 debug layer.</span></span> <span data-ttu-id="05c1e-115">*Quindi* abilitare il livello di debug DirectML chiamando **DMLCreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="05c1e-115">And *then* enable the DirectML debug layer by calling **DMLCreateDevice**.</span></span>

<span data-ttu-id="05c1e-116">Dopo aver abilitato il livello di debug DirectML, gli eventuali errori DirectML o chiamate API non valide comporteranno la creazione di informazioni di debug come output di debug.</span><span class="sxs-lookup"><span data-stu-id="05c1e-116">Once you've enabled the DirectML debug layer, any DirectML errors or invalid API calls will cause debugging information to be emitted as debug output.</span></span> <span data-ttu-id="05c1e-117">Ecco un esempio.</span><span class="sxs-lookup"><span data-stu-id="05c1e-117">Here's an example.</span></span>

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a><span data-ttu-id="05c1e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05c1e-118">See also</span></span>

* [<span data-ttu-id="05c1e-119">DMLCreateDevice (funzione)</span><span class="sxs-lookup"><span data-stu-id="05c1e-119">DMLCreateDevice function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [<span data-ttu-id="05c1e-120">Funzionalità disponibili su richiesta</span><span class="sxs-lookup"><span data-stu-id="05c1e-120">Available Features-on-Demand</span></span>](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [<span data-ttu-id="05c1e-121">Usare la convalida basata su GPU con il livello di debug Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="05c1e-121">Use GPU-based validation with the Direct3D 12 Debug Layer</span></span>](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [<span data-ttu-id="05c1e-122">Riferimento al livello di debug Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="05c1e-122">Direct3D 12 Debug Layer reference</span></span>](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
