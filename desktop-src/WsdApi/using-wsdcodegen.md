---
description: Descrive il processo di compilazione di un'applicazione WSDAPI usando WsdCodeGen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Uso di WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312672"
---
# <a name="using-wsdcodegen"></a><span data-ttu-id="34c3e-103">Uso di WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="34c3e-103">Using WsdCodeGen</span></span>

<span data-ttu-id="34c3e-104">**Per compilare un'applicazione WSDAPI usando WsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="34c3e-104">**To build a WSDAPI application using WsdCodeGen**</span></span>

1.  <span data-ttu-id="34c3e-105">Definire il contratto funzionale per l'host del dispositivo in un file WSDL.</span><span class="sxs-lookup"><span data-stu-id="34c3e-105">Define the functional contract for the device host in a WSDL file.</span></span>
2.  <span data-ttu-id="34c3e-106">Generare un file di configurazione usando WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="34c3e-106">Generate a configuration file using WsdCodeGen.</span></span> <span data-ttu-id="34c3e-107">Per altre informazioni, vedere [file di configurazione di WsdCodeGen](wsdcodegen-configuration-file.md) e [sintassi della riga di comando di WsdCodeGen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="34c3e-107">For more information, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md) and [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
3.  <span data-ttu-id="34c3e-108">Aprire il file di configurazione generato e modificare il file in modo che sia necessario.</span><span class="sxs-lookup"><span data-stu-id="34c3e-108">Open the generated configuration file and modify the file as required.</span></span> <span data-ttu-id="34c3e-109">Se si sta compilando un'applicazione client, è necessaria una modifica minima o nulla.</span><span class="sxs-lookup"><span data-stu-id="34c3e-109">If you are building a client application, little or no modification is required.</span></span> <span data-ttu-id="34c3e-110">Se si compila un'applicazione host, modificare gli elementi di configurazione specifici dell'utente, ad esempio [**Manufacturer**](manufacturer.md) e [**ModelName**](modelname.md).</span><span class="sxs-lookup"><span data-stu-id="34c3e-110">If you are building a host application, change the user-specific configuration elements (such as [**manufacturer**](manufacturer.md) and [**modelName**](modelname.md)).</span></span>
4.  <span data-ttu-id="34c3e-111">Generare il codice usando WsdCodeGen, specificando il file di configurazione come input.</span><span class="sxs-lookup"><span data-stu-id="34c3e-111">Generate code using WsdCodeGen, providing the configuration file as input.</span></span> <span data-ttu-id="34c3e-112">Per ulteriori informazioni, vedere [sintassi della riga di comando WsdCodeGen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="34c3e-112">For more information, see [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
5.  <span data-ttu-id="34c3e-113">Usare il codice generato per compilare un client, un host o entrambi.</span><span class="sxs-lookup"><span data-stu-id="34c3e-113">Use the generated code to build a client, host, or both.</span></span>

<span data-ttu-id="34c3e-114">Il Windows SDK include alcuni file WSDL di esempio, i file di configurazione WsdCodeGen e il codice generato.</span><span class="sxs-lookup"><span data-stu-id="34c3e-114">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="34c3e-115">Per ulteriori informazioni, vedere [WSDAPI Samples](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="34c3e-115">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="34c3e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34c3e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34c3e-117">Esempi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="34c3e-117">WSDAPI Samples</span></span>](wsdapi-samples.md)
</dt> </dl>

 

 



