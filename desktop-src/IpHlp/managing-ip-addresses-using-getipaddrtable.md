---
description: La funzione GetIpAddrTable compila un puntatore a una \_ struttura IPADDRTABLE MIB con informazioni sugli indirizzi IP correnti associati al sistema.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Gestione degli indirizzi IP tramite GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881518"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a><span data-ttu-id="22664-103">Gestione degli indirizzi IP tramite GetIpAddrTable</span><span class="sxs-lookup"><span data-stu-id="22664-103">Managing IP Addresses Using GetIpAddrTable</span></span>

<span data-ttu-id="22664-104">La funzione [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) compila un puntatore a una struttura [**\_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) con informazioni sugli indirizzi IP correnti associati al sistema.</span><span class="sxs-lookup"><span data-stu-id="22664-104">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function fills a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) structure with information about the current IP addresses associated with the system.</span></span>

<span data-ttu-id="22664-105">**Per usare GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="22664-105">**To use GetIpAddrTable**</span></span>

1.  <span data-ttu-id="22664-106">Dichiarare un puntatore a un [**oggetto \_ MIB IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) denominato *PIPAddrTable* e un oggetto **DWORD** denominato *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="22664-106">Declare a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) object called *pIPAddrTable*, and a **DWORD** object called *dwSize*.</span></span> <span data-ttu-id="22664-107">Queste variabili vengono passate come parametri alla funzione [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) .</span><span class="sxs-lookup"><span data-stu-id="22664-107">These variables are passed as parameters to the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="22664-108">Creare anche una variabile **DWORD** denominata *dwRetVal* (usata per il controllo degli errori).</span><span class="sxs-lookup"><span data-stu-id="22664-108">Also create a **DWORD** variable called *dwRetVal* (used for error checking).</span></span>
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="22664-109">Allocare memoria per la struttura.</span><span class="sxs-lookup"><span data-stu-id="22664-109">Allocate memory for the structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="22664-110">Le dimensioni di *dwSize* non sono sufficienti per conservare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="22664-110">The size of *dwSize* is not sufficient to hold the information.</span></span> <span data-ttu-id="22664-111">Vedere il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="22664-111">See the next step.</span></span>

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  <span data-ttu-id="22664-112">Eseguire una chiamata iniziale a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) per ottenere le dimensioni necessarie nella variabile *dwSize* .</span><span class="sxs-lookup"><span data-stu-id="22664-112">Make an initial call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) to get the size needed into the *dwSize* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="22664-113">Questa chiamata alla funzione deve avere esito negativo e viene usata per garantire che la variabile *dwSize* specifichi una dimensione sufficiente per contenere tutte le informazioni restituite a *pIPAddrTable*.</span><span class="sxs-lookup"><span data-stu-id="22664-113">This call to the function is meant to fail, and is used to ensure that the *dwSize* variable specifies a size sufficient for holding all the information returned to *pIPAddrTable*.</span></span> <span data-ttu-id="22664-114">Si tratta di un modello di programmazione comune per le strutture di dati e le funzioni di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="22664-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  <span data-ttu-id="22664-115">Eseguire una seconda chiamata a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) con il controllo generale degli errori e restituirne il valore alla variabile **DWORD** *dwRetVal* (per un controllo degli errori più avanzato).</span><span class="sxs-lookup"><span data-stu-id="22664-115">Make a second call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) with general error checking and return its value to the **DWORD** variable *dwRetVal* (for more advanced error checking).</span></span>
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  <span data-ttu-id="22664-116">Se la chiamata ha avuto esito positivo, accedere ai dati dalla struttura di dati *pIPAddrTable* .</span><span class="sxs-lookup"><span data-stu-id="22664-116">If the call was successful, access the data from the *pIPAddrTable* data structure.</span></span>
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  <span data-ttu-id="22664-117">Liberare la memoria allocata per la struttura *pIPAddrTable* .</span><span class="sxs-lookup"><span data-stu-id="22664-117">Free any memory allocated for the *pIPAddrTable* structure.</span></span>
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> <span data-ttu-id="22664-118">Gli  oggetti DWORD *dwAddr* e *dwMask* vengono restituiti come valori numerici nell'ordine dei byte dell'host, non nell'ordine dei byte di rete.</span><span class="sxs-lookup"><span data-stu-id="22664-118">The **DWORD** objects *dwAddr* and *dwMask* are returned as numerical values in host byte order, not network byte order.</span></span> <span data-ttu-id="22664-119">Questi valori non sono indirizzi IP punteggiati.</span><span class="sxs-lookup"><span data-stu-id="22664-119">These values are not dotted IP addresses.</span></span>

 

<span data-ttu-id="22664-120">Passaggio successivo: [gestione dei lease DHCP con IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="22664-120">Next Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

<span data-ttu-id="22664-121">Passaggio precedente: [gestione delle interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="22664-121">Previous Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

 

 
