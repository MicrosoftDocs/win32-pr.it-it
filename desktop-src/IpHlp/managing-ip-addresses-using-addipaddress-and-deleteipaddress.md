---
title: Gestire gli indirizzi IP con AddIPAddress, DeleteIPAddress
description: La funzione AddIPAddress aggiunge l'indirizzo IPv4 specificato all'adapter specificato.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311751"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a><span data-ttu-id="3627c-103">Gestire gli indirizzi IP con AddIPAddress, DeleteIPAddress</span><span class="sxs-lookup"><span data-stu-id="3627c-103">Manage IP addresses with AddIPAddress, DeleteIPAddress</span></span>

<span data-ttu-id="3627c-104">La funzione [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) aggiunge l'indirizzo IPv4 specificato all'adapter specificato.</span><span class="sxs-lookup"><span data-stu-id="3627c-104">The [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function adds the specified IPv4 address to the specified adapter.</span></span> <span data-ttu-id="3627c-105">La funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) Elimina l'indirizzo IPv4 specificato dall'adapter specificato.</span><span class="sxs-lookup"><span data-stu-id="3627c-105">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function deletes the specified IPv4 address from the specified adapter.</span></span> <span data-ttu-id="3627c-106">Queste funzioni possono essere utilizzate per aggiungere ed eliminare indirizzi IPv4 a una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="3627c-106">These functions can be used to add and delete IPv4 addresses to a network adapter.</span></span>

<span data-ttu-id="3627c-107">Un indirizzo IPv4 aggiunto dalla funzione [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) non è persistente.</span><span class="sxs-lookup"><span data-stu-id="3627c-107">An IPv4 address added by the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function is not persistent.</span></span> <span data-ttu-id="3627c-108">L'indirizzo IPv4 esiste solo fino a quando l'oggetto adapter esiste.</span><span class="sxs-lookup"><span data-stu-id="3627c-108">The IPv4 address exists only as long as the adapter object exists.</span></span> <span data-ttu-id="3627c-109">Il riavvio del computer comporta l'eliminazione dell'indirizzo IPv4, così come si ripristina manualmente la scheda di interfaccia di rete (NIC).</span><span class="sxs-lookup"><span data-stu-id="3627c-109">Restarting the computer destroys the IPv4 address, as does manually resetting the network interface card (NIC).</span></span>

<span data-ttu-id="3627c-110">Dopo che [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) è stato chiamato correttamente, DHCP verrà disabilitato per l'indirizzo IP aggiunto.</span><span class="sxs-lookup"><span data-stu-id="3627c-110">After [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) has been called successfully, DHCP will be disabled for the IP address that was added.</span></span> <span data-ttu-id="3627c-111">Pertanto, le funzioni come [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), che richiedono l'abilitazione di DHCP, non funzioneranno sull'indirizzo IP aggiunto.</span><span class="sxs-lookup"><span data-stu-id="3627c-111">Therefore, functions such as [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), which require DHCP to be enabled, will not be functional on the added IP address.</span></span> <span data-ttu-id="3627c-112">Per eliminare l'indirizzo IPv4 aggiunto, è possibile utilizzare la funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .</span><span class="sxs-lookup"><span data-stu-id="3627c-112">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function can be used to delete the added IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="3627c-113">Criteri di gruppo, criteri aziendali e altre restrizioni sulla rete possono impedire il corretto completamento di queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="3627c-113">Group policies, enterprise policies, and other restrictions on the network may prevent these functions from completing successfully.</span></span> <span data-ttu-id="3627c-114">Assicurarsi che l'applicazione disponga delle autorizzazioni di rete necessarie prima di provare a usare queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="3627c-114">Ensure that the application has the necessary network permissions before attempting to use these functions.</span></span>

 

<span data-ttu-id="3627c-115">**Per usare AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="3627c-115">**To use AddIPAddress**</span></span>

1.  <span data-ttu-id="3627c-116">Dichiarare le variabili **ULONG** denominate `NTEContext` e `NTEInstance` , entrambe inizializzate su zero.</span><span class="sxs-lookup"><span data-stu-id="3627c-116">Declare **ULONG** variables named `NTEContext` and `NTEInstance`, both initialized to zero.</span></span>
    > [!Note]  
    > <span data-ttu-id="3627c-117">La `NTEContext` variabile è l'unico parametro per la funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) . per eliminare l'indirizzo IP aggiunto, `NTEContext` deve essere archiviato e non modificato.</span><span class="sxs-lookup"><span data-stu-id="3627c-117">The `NTEContext` variable is the only parameter to the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function; to delete the IP address that is added, `NTEContext` must be stored and unchanged.</span></span>

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  <span data-ttu-id="3627c-118">Dichiarare le variabili per le strutture IPAddr e IPMask denominate `iaIPAddress` `iaIPMask` rispettivamente e.</span><span class="sxs-lookup"><span data-stu-id="3627c-118">Declare variables for the IPAddr and IPMask structures named `iaIPAddress` and `iaIPMask`, respectively.</span></span> <span data-ttu-id="3627c-119">Questi valori sono semplicemente interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="3627c-119">These values are simply unsigned integers.</span></span> <span data-ttu-id="3627c-120">Inizializzare `iaIPAddress` le `iaIPMask` variabili e mediante la funzione [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .</span><span class="sxs-lookup"><span data-stu-id="3627c-120">Initialize the `iaIPAddress` and `iaIPMask` variables using the [**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) function.</span></span>
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  <span data-ttu-id="3627c-121">Chiamare la funzione [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per aggiungere l'indirizzo IPv4.</span><span class="sxs-lookup"><span data-stu-id="3627c-121">Call the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add the IPv4 address.</span></span> <span data-ttu-id="3627c-122">Verificare la presenza di errori e restituire il valore di errore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più completo).</span><span class="sxs-lookup"><span data-stu-id="3627c-122">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > <span data-ttu-id="3627c-123">Il terzo parametro è l'indice dell'adattatore, che può essere ottenuto chiamando la funzione [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="3627c-123">The third parameter is the adapter index, which can be obtained by calling the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="3627c-124">Si presuppone che la variabile restituita da questa funzione sia denominata `pIPAddrTable` .</span><span class="sxs-lookup"><span data-stu-id="3627c-124">It is assumed that the variable returned by this function is named `pIPAddrTable`.</span></span> <span data-ttu-id="3627c-125">Per informazioni sulla funzione **GetIpAddrTable** , vedere [Managing IP address using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="3627c-125">For help with the **GetIpAddrTable** function, see [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

     

<span data-ttu-id="3627c-126">**Per usare DeleteIpAddress**</span><span class="sxs-lookup"><span data-stu-id="3627c-126">**To use DeleteIpAddress**</span></span>

-   <span data-ttu-id="3627c-127">Chiamare la funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , passando la `NTEContext` variabile come parametro.</span><span class="sxs-lookup"><span data-stu-id="3627c-127">Call the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function, passing the `NTEContext` variable as its parameter.</span></span> <span data-ttu-id="3627c-128">Verificare la presenza di errori e restituire il valore di errore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più completo).</span><span class="sxs-lookup"><span data-stu-id="3627c-128">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> <span data-ttu-id="3627c-129">Per usare [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), è prima necessario chiamare [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per ottenere l'handle `NTEContext` .</span><span class="sxs-lookup"><span data-stu-id="3627c-129">To use [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) must first be called to get the handle `NTEContext`.</span></span> <span data-ttu-id="3627c-130">Nella procedura precedente si presuppone che **AddIpAddress** sia già stato chiamato in un punto qualsiasi del codice ed `NTEContext` è stato salvato e rimane inalterato.</span><span class="sxs-lookup"><span data-stu-id="3627c-130">The previous procedure assumes that **AddIPAddress** has already been called somewhere in the code, and `NTEContext` has been saved and remains uncorrupted.</span></span>

 

<span data-ttu-id="3627c-131">Passaggio successivo: [recupero di informazioni tramite GetIPStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="3627c-131">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="3627c-132">Passaggio precedente: [gestione dei lease DHCP con IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="3627c-132">Previous Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

 

 
