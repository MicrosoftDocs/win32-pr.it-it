---
description: La procedura seguente fornisce una breve panoramica del processo di compilazione.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Compilazione di un comando ISO7816-4 APDU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226486"
---
# <a name="building-an-iso7816-4-apdu-command"></a><span data-ttu-id="bd21c-103">Compilazione di un comando ISO7816-4 APDU</span><span class="sxs-lookup"><span data-stu-id="bd21c-103">Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="bd21c-104">Per aggiungere funzionalità a un provider di servizi, è necessario capire come viene compilata un' [*unità dati del protocollo*](/windows/desktop/SecGloss/a-gly) ISO7816-4 (APDU) all'interno delle dll del provider di servizi di base.</span><span class="sxs-lookup"><span data-stu-id="bd21c-104">To add functionality to a service provider, you need to know how an ISO7816-4 [*application protocol data unit*](/windows/desktop/SecGloss/a-gly) (APDU) is built within the base service provider DLLs.</span></span> <span data-ttu-id="bd21c-105">La procedura seguente fornisce una breve panoramica del processo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="bd21c-105">The following procedure gives a brief overview of the build process.</span></span>

> [!Note]  
> <span data-ttu-id="bd21c-106">L'esempio incluso in questo argomento non è necessariamente completo; Per ulteriori informazioni, vedere le applicazioni e le DLL di esempio.</span><span class="sxs-lookup"><span data-stu-id="bd21c-106">The example included here is not necessarily complete; for more information, see the sample applications and DLLs.</span></span>

 

<span data-ttu-id="bd21c-107">**Per compilare un comando ISO7816-4 APDU**</span><span class="sxs-lookup"><span data-stu-id="bd21c-107">**To build an ISO7816-4 APDU command**</span></span>

1.  <span data-ttu-id="bd21c-108">Creare un oggetto [**ISCardCmd**](iscardcmd.md) e un oggetto [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="bd21c-108">Create an [**ISCardCmd**](iscardcmd.md) object and an [**ISCardISO7816**](iscardiso7816.md) object.</span></span>

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    <span data-ttu-id="bd21c-109">L'interfaccia [**ISCardCmd**](iscardcmd.md) contiene due buffer **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="bd21c-109">The [**ISCardCmd**](iscardcmd.md) interface contains two **IByteBuffer** buffers.</span></span> <span data-ttu-id="bd21c-110">Un buffer contiene la stringa di comando APDU effettiva, più tutti i dati da inviare con il comando.</span><span class="sxs-lookup"><span data-stu-id="bd21c-110">One buffer contains the actual APDU command string (plus any data to send with the command).</span></span> <span data-ttu-id="bd21c-111">L'altra contiene le informazioni di risposta restituite dalla scheda dopo l'esecuzione del comando.</span><span class="sxs-lookup"><span data-stu-id="bd21c-111">The other contains any reply information returned by the card after command execution.</span></span>

2.  <span data-ttu-id="bd21c-112">Usando questi oggetti, creare un comando ISO7816-4 valido come segue:</span><span class="sxs-lookup"><span data-stu-id="bd21c-112">Using these objects, create a valid ISO7816-4 command as follows:</span></span>

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    <span data-ttu-id="bd21c-113">Ecco il codice usato nel metodo [**getchallenge**](iscardiso7816-getchallenge.md) :</span><span class="sxs-lookup"><span data-stu-id="bd21c-113">Here is the code used in the [**GetChallenge**](iscardiso7816-getchallenge.md) method:</span></span>

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    <span data-ttu-id="bd21c-114">Il metodo [**ISCardISO7816:: getchallenge**](iscardiso7816-getchallenge.md) usa il metodo [**ISCardCmd:: BuildCmd**](iscardcmd-buildcmd.md) per compilare la APDU richiesta.</span><span class="sxs-lookup"><span data-stu-id="bd21c-114">The [**ISCardISO7816::GetChallenge**](iscardiso7816-getchallenge.md) method uses the [**ISCardCmd::BuildCmd**](iscardcmd-buildcmd.md) method to build the requested APDU.</span></span> <span data-ttu-id="bd21c-115">Questa operazione viene eseguita scrivendo le informazioni appropriate nel buffer APDU di [**ISCardCmd**](iscardcmd.md) nell'istruzione seguente:</span><span class="sxs-lookup"><span data-stu-id="bd21c-115">This is done by writing the appropriate information into the [**ISCardCmd**](iscardcmd.md) APDU buffer in the following statement:</span></span>

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  <span data-ttu-id="bd21c-116">Utilizzando l'oggetto [**ISCardCmd**](iscardcmd.md) compilato, eseguire una transazione con la scheda, interpretare i risultati e continuare.</span><span class="sxs-lookup"><span data-stu-id="bd21c-116">Using the built [**ISCardCmd**](iscardcmd.md) object, do a transaction with the card, interpret the results, and continue.</span></span>

## <a name="expanding-beyond-iso7816-4"></a><span data-ttu-id="bd21c-117">Espansione oltre ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="bd21c-117">Expanding Beyond ISO7816-4</span></span>

<span data-ttu-id="bd21c-118">Il metodo consigliato per espandere il processo di compilazione/esecuzione del provider di servizi descritto in precedenza consiste nel creare un nuovo oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="bd21c-118">The recommended way to expand the service provider build/execute process described above is to create a new COM object.</span></span> <span data-ttu-id="bd21c-119">Questo oggetto COM deve supportare una nuova interfaccia che consente la creazione di comandi non ISO7816-4 e deve aggregare l'interfaccia [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="bd21c-119">This COM object should support a new interface that allows creation of non-ISO7816-4 commands and should aggregate the [**ISCardISO7816**](iscardiso7816.md) interface.</span></span>

## <a name="example-of-building-an-iso7816-4-apdu-command"></a><span data-ttu-id="bd21c-120">Esempio di compilazione di un comando ISO7816-4 APDU</span><span class="sxs-lookup"><span data-stu-id="bd21c-120">Example of Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="bd21c-121">Nell'esempio seguente viene illustrato il codice utilizzato nella procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="bd21c-121">The following example shows the code used in the procedure above.</span></span>


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 
