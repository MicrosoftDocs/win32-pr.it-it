---
description: Ottiene i dati non elaborati per una struttura di dati di identificazione estesa (EDID) avanzata di video Electronics Standard Association (VESA) che definisce le impostazioni ottimali per la configurazione di un monitoraggio.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Metodo WmiGetMonitorRawEEdidV1Block della classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316586"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a><span data-ttu-id="0d940-103">Metodo WmiGetMonitorRawEEdidV1Block della classe WmiMonitorDescriptorMethods</span><span class="sxs-lookup"><span data-stu-id="0d940-103">WmiGetMonitorRawEEdidV1Block method of the WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="0d940-104">Il metodo **WmiGetMonitorRawEEdidV1Block** ottiene i dati non elaborati per una struttura di EDID (video Electronics Standard Association) avanzata (VESA) migliorata che definisce le impostazioni ottimali per la configurazione di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="0d940-104">The **WmiGetMonitorRawEEdidV1Block** method gets the raw data for a specified Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure that defines optimal settings for configuring a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d940-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d940-105">Syntax</span></span>


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a><span data-ttu-id="0d940-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d940-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d940-107">*ID blocco* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d940-107">*BlockId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d940-108">Identità del blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="0d940-108">The data block identity.</span></span>

</dd> <dt>

<span data-ttu-id="0d940-109">*BlockType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d940-109">*BlockType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d940-110">Tipo di blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="0d940-110">Type of data block.</span></span> <span data-ttu-id="0d940-111">Nella tabella seguente sono elencati i valori restituiti possibili.</span><span class="sxs-lookup"><span data-stu-id="0d940-111">The following table lists possible return values.</span></span>



| <span data-ttu-id="0d940-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0d940-112">Value</span></span>                                                                                 | <span data-ttu-id="0d940-113">Significato</span><span class="sxs-lookup"><span data-stu-id="0d940-113">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="0d940-114"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0d940-114"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="0d940-115">Inizializzazione annullata</span><span class="sxs-lookup"><span data-stu-id="0d940-115">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="0d940-116"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0d940-116"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="0d940-117">Blocco base EDID</span><span class="sxs-lookup"><span data-stu-id="0d940-117">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="0d940-118"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0d940-118"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="0d940-119">Mappa di blocco EDID</span><span class="sxs-lookup"><span data-stu-id="0d940-119">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="0d940-120"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="0d940-120"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="0d940-121">Altro</span><span class="sxs-lookup"><span data-stu-id="0d940-121">Other</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="0d940-122">*BlockContent* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d940-122">*BlockContent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d940-123">Matrice di 128 byte che contiene il contenuto del blocco non elaborato.</span><span class="sxs-lookup"><span data-stu-id="0d940-123">A 128-byte array that contains the raw block content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d940-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d940-124">Return value</span></span>

<span data-ttu-id="0d940-125">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0d940-125">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="0d940-126">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="0d940-126">Any other number indicates an error.</span></span> <span data-ttu-id="0d940-127">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0d940-127">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="0d940-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="0d940-128">Examples</span></span>

<span data-ttu-id="0d940-129">Nell'esempio di codice seguente vengono recuperati i blocchi EDID di qualsiasi visualizzazione come matrici di bit 128 non elaborate.</span><span class="sxs-lookup"><span data-stu-id="0d940-129">The following code example retrieves the EDID blocks of any display as raw 128 bit arrays.</span></span>


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="0d940-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d940-130">Requirements</span></span>



| <span data-ttu-id="0d940-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d940-131">Requirement</span></span> | <span data-ttu-id="0d940-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0d940-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d940-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d940-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0d940-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d940-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0d940-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d940-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0d940-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d940-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0d940-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d940-137">Namespace</span></span><br/>                | <span data-ttu-id="0d940-138">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="0d940-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="0d940-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0d940-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d940-140"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d940-140"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d940-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0d940-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d940-142"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d940-142"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d940-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d940-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d940-144">**WmiMonitorDescriptorMethods**</span><span class="sxs-lookup"><span data-stu-id="0d940-144">**WmiMonitorDescriptorMethods**</span></span>](wmimonitordescriptormethods.md)
</dt> <dt>

[<span data-ttu-id="0d940-145">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="0d940-145">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

