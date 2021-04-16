---
description: I certificati possono essere aggiunti o rimossi dagli archivi certificati se l'archivio viene aperto con l'autorizzazione di lettura/scrittura.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Aggiunta di certificati a un archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529233"
---
# <a name="adding-certificates-to-a-certificate-store"></a><span data-ttu-id="db780-103">Aggiunta di certificati a un archivio certificati</span><span class="sxs-lookup"><span data-stu-id="db780-103">Adding Certificates to a Certificate Store</span></span>

<span data-ttu-id="db780-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db780-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="db780-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="db780-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="db780-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="db780-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="db780-107">I [*certificati*](../secgloss/c-gly.md) possono essere aggiunti o rimossi dagli [*archivi certificati*](../secgloss/c-gly.md) se l'archivio viene aperto con l'autorizzazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="db780-107">[*Certificates*](../secgloss/c-gly.md) can be added to or removed from [*certificate stores*](../secgloss/c-gly.md) if the store is opened with read/write permission.</span></span> <span data-ttu-id="db780-108">L'autorizzazione di lettura/scrittura non è concessa per gli archivi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db780-108">Read/write permission is not granted to Active Directory stores.</span></span> <span data-ttu-id="db780-109">Mentre i certificati possono essere aggiunti o rimossi dagli archivi di memoria, le modifiche negli archivi di memoria non vengono rese permanente tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="db780-109">While certificates can be added to or removed from memory stores, changes in memory stores are not persisted between sessions.</span></span>

<span data-ttu-id="db780-110">I certificati possono essere aggiunti a un archivio certificati aperto con l'autorizzazione di lettura/scrittura tramite il metodo **Add** .</span><span class="sxs-lookup"><span data-stu-id="db780-110">Certificates can be added to a certificate store that is opened with read/write permission by using the **Add** method.</span></span> <span data-ttu-id="db780-111">È possibile rimuovere un certificato da un archivio certificati aperto con l'autorizzazione di lettura/scrittura tramite il metodo **Remove** .</span><span class="sxs-lookup"><span data-stu-id="db780-111">A certificate can be removed from a certificate store that is opened with read/write permission by using the **Remove** method.</span></span> <span data-ttu-id="db780-112">I nuovi archivi possono essere creati e salvati nell' \_ \_ Archivio dell'utente corrente di CAPICOM e nei percorsi di \_ \_ \_ archiviazione del computer locale \_ .</span><span class="sxs-lookup"><span data-stu-id="db780-112">New stores can be created and saved in the CAPICOM\_CURRENT\_USER\_STORE and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="db780-113">Gli archivi appena creati in uno di questi percorsi possono essere aperti con l'autorizzazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="db780-113">Newly created stores in either of these locations can be opened with read/write permission.</span></span>

<span data-ttu-id="db780-114">Nell'esempio seguente vengono aperti due archivi certificati.</span><span class="sxs-lookup"><span data-stu-id="db780-114">In the following example, two certificate stores are opened.</span></span> <span data-ttu-id="db780-115">I certificati di oggetti con i cognomi che iniziano con F vengono recuperati dall'archivio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db780-115">Certificates of subjects with last names beginning with F are retrieved from the Active Directory store.</span></span> <span data-ttu-id="db780-116">L'archivio dell' \_ utente corrente di CAPICOM \_ , l' \_ Archivio dell' \_ archivio CA CAPICOM \_ viene quindi aperto come archivio di lettura/scrittura e il primo certificato della raccolta di certificati nell'archivio Active Directory viene aggiunto ai certificati nell' \_ Archivio della CA CAPICOM \_ .</span><span class="sxs-lookup"><span data-stu-id="db780-116">The CAPICOM\_CURRENT\_USER\_STORE, CAPICOM\_CA\_STORE store is then opened as a read/write store and the first certificate from the collection of certificates in the Active Directory store is added to the certificates in the CAPICOM\_CA\_STORE.</span></span>

<span data-ttu-id="db780-117">A scopo dimostrativo, l'esempio mostra l'apertura di archivi nell'archivio di \_ memoria CAPICOM \_ , l' \_ \_ Archivio dell'utente corrente di CAPICOM e i percorsi di \_ \_ \_ archiviazione del computer locale \_ di CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="db780-117">For demonstration purposes, the example shows the opening of stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="db780-118">Nell'esempio viene illustrata l'esportazione di tutti i certificati da un archivio aperto, la scrittura dei certificati esportati in un file, la relativa lettura e l'importazione in un altro archivio.</span><span class="sxs-lookup"><span data-stu-id="db780-118">The example shows exporting all certificates from an open store, writing the exported certificates to a file, reading them back in, and importing them into a different store.</span></span> <span data-ttu-id="db780-119">I certificati appena importati vengono enumerati e visualizzati.</span><span class="sxs-lookup"><span data-stu-id="db780-119">The newly imported certificates are them enumerated and displayed.</span></span>

<span data-ttu-id="db780-120">In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="db780-120">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="db780-121">Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="db780-121">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="db780-122">Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="db780-122">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="db780-123">Nell'esempio seguente viene illustrata l'apertura di archivi certificati mediante associazione anticipata nella dichiarazione degli oggetti **Archivio** e nella creazione di un'istanza di tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="db780-123">The following example shows opening certificate stores using early binding in the declaration of the **Store** objects and in creating an instance of those objects.</span></span>


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
