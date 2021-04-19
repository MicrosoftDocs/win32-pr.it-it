---
description: Nell'esempio seguente, i certificati in un archivio locale vengono enumerati e controllati per verificarne la validità.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Raccolta e verifica dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0b160f373d5ade65679fcc4dd87e3c1c86dc4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309982"
---
# <a name="collecting-and-verifying-certificates"></a><span data-ttu-id="d17d2-103">Raccolta e verifica dei certificati</span><span class="sxs-lookup"><span data-stu-id="d17d2-103">Collecting and Verifying Certificates</span></span>

<span data-ttu-id="d17d2-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d17d2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d17d2-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d17d2-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="d17d2-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="d17d2-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="d17d2-107">Spesso è necessario raccogliere e verificare un gruppo di [*certificati*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d17d2-107">Often a group of [*certificates*](../secgloss/c-gly.md) needs to be collected and verified.</span></span> <span data-ttu-id="d17d2-108">Questa operazione può essere eseguita spesso per preparare un gruppo di destinatari per un messaggio in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="d17d2-108">This would often be done to prepare a group of recipients for an enveloped message.</span></span> <span data-ttu-id="d17d2-109">Nell'esempio seguente, i certificati in un archivio locale vengono enumerati e controllati per verificarne la validità.</span><span class="sxs-lookup"><span data-stu-id="d17d2-109">In the example that follows, the certificates in a local store are enumerated and checked for validity.</span></span> <span data-ttu-id="d17d2-110">Viene quindi aperto un archivio Active Directory per recuperare e aggiungere i nuovi certificati dell'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="d17d2-110">Next, an Active Directory store is opened to retrieve and add to the local store new certificates.</span></span> <span data-ttu-id="d17d2-111">Viene verificata la validità dei certificati recuperati dall'archivio di Active Directory e, se validi, vengono aggiunti all'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="d17d2-111">The certificates retrieved from the active directory store are checked for validity and, if valid, are added to the local store.</span></span> <span data-ttu-id="d17d2-112">Entrambi gli archivi vengono quindi chiusi.</span><span class="sxs-lookup"><span data-stu-id="d17d2-112">Both stores are then closed.</span></span>

<span data-ttu-id="d17d2-113">In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="d17d2-113">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="d17d2-114">Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="d17d2-114">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="d17d2-115">Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="d17d2-115">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="d17d2-116">In questo esempio, il nome dell'archivio locale viene passato come parametro di stringa.</span><span class="sxs-lookup"><span data-stu-id="d17d2-116">In this example, the name of the local store is passed in as a string parameter.</span></span> <span data-ttu-id="d17d2-117">Una stringa che indica i criteri di ricerca per i certificati nell'archivio Active Directory viene passata anche come parametro.</span><span class="sxs-lookup"><span data-stu-id="d17d2-117">A string indicating the search criteria for certificates in the Active Directory store is also passed in as a parameter.</span></span>


```VB
Sub CollectValidCerts(ByVal storename As String, ByVal _
    certname As String)

    On Error GoTo errorhandler

    ' Prepare a local certificate store to contain valid
    ' certificates for the recipients of an enveloped
    ' message.

    ' Open the local store and go to the certificates in the store
    '   1. Display the certificate
    '   2. Check the validity of the certificate
    '   3. Remove certificates that are not valid from the store

    Dim LocalStore As New Store
    Dim ADStore As New Store
    Dim i As Long

    LocalStore.Open(CAPICOM_CURRENT_USER_STORE, storename, _
        CAPICOM_STORE_OPEN_READ_WRITE)

    MsgBox("There are " & LocalStore.Certificates.Count & _
        " certificates in this store ")
    For i = 1 To LocalStore.Certificates.Count
        If LocalStore.Certificates.Item(i).IsValid Then
            LocalStore.Certificates.Item(i).Display()
        Else
            MsgBox("A certificate that is not valid was found.")
        End If
    Next i

    ' Open the AD store and retrieve a certificate based
    ' on a string passed into the function. Add any valid
    ' certificates found to the local store.

    ADStore.Open(CAPICOM_ACTIVE_DIRECTORY_USER_STORE, certname, _
        CAPICOM_STORE_OPEN_READ_ONLY)
    MsgBox("There are " & ADStore.Certificates.Count & _
        " certificates in the AD store.")

    For i = 1 To ADStore.Certificates.Count
        If ADStore.Certificates.Item(i).IsValid Then
            ADStore.Certificates.Item(i).Display()
            LocalStore.Add(ADStore.Certificates.Item(i))
        Else
            MsgBox("the certificate from the AD store is not valid.")
        End If
    Next i

    LocalStore = Nothing
    ADStore = Nothing
    MsgBox("Sub finished without error ")
    Exit Sub
errorhandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
