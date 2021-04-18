---
description: Le interfacce seguenti possono essere utilizzate per registrare un utente o un computer in una gerarchia di certificati.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Interfacce di registrazione certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318961"
---
# <a name="certificate-enrollment-interfaces"></a><span data-ttu-id="9abed-103">Interfacce di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="9abed-103">Certificate Enrollment Interfaces</span></span>

<span data-ttu-id="9abed-104">Le interfacce seguenti possono essere utilizzate per registrare un utente o un computer in una gerarchia di certificati.</span><span class="sxs-lookup"><span data-stu-id="9abed-104">The following interfaces can be used to enroll a user or a computer in a certificate hierarchy.</span></span>



| <span data-ttu-id="9abed-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="9abed-105">Interface</span></span>                                              | <span data-ttu-id="9abed-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9abed-106">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9abed-107">**Metodo IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="9abed-107">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | <span data-ttu-id="9abed-108">Registra un computer o un utente in una gerarchia di certificati.</span><span class="sxs-lookup"><span data-stu-id="9abed-108">Enrolls a computer or user in a certificate hierarchy.</span></span>                                                                                                                              |
| [<span data-ttu-id="9abed-109">**IX509Enrollment2**</span><span class="sxs-lookup"><span data-stu-id="9abed-109">**IX509Enrollment2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | <span data-ttu-id="9abed-110">Estende l'interfaccia [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) per abilitare l'inizializzazione da un modello.</span><span class="sxs-lookup"><span data-stu-id="9abed-110">Extends the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to enable initialization from a template.</span></span>                                                                          |
| [<span data-ttu-id="9abed-111">**IX509EnrollmentHelper**</span><span class="sxs-lookup"><span data-stu-id="9abed-111">**IX509EnrollmentHelper**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | <span data-ttu-id="9abed-112">Definisce i metodi che consentono a un'applicazione Web di registrare un certificato, archiviare le credenziali del server dei criteri nella cache delle credenziali e registrare i server dei criteri e i server di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9abed-112">Defines methods that enable a web application to enroll a certificate, store policy server credentials in the credential cache, and register policy servers and enrollment servers.</span></span> |
| [<span data-ttu-id="9abed-113">**IX509EnrollmentStatus**</span><span class="sxs-lookup"><span data-stu-id="9abed-113">**IX509EnrollmentStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | <span data-ttu-id="9abed-114">Recupera informazioni dettagliate sugli errori relativi a una transazione di registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="9abed-114">Retrieves detailed error information about a certificate enrollment transaction.</span></span>                                                                                                    |
| [<span data-ttu-id="9abed-115">**IX509SCEPEnrollment**</span><span class="sxs-lookup"><span data-stu-id="9abed-115">**IX509SCEPEnrollment**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | <span data-ttu-id="9abed-116">Interfaccia del protocollo di registrazione del computer semplice X. 509</span><span class="sxs-lookup"><span data-stu-id="9abed-116">X.509 Simple Computer Enrollment Protocol Interface</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="9abed-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9abed-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9abed-118">Interfacce CertEnroll</span><span class="sxs-lookup"><span data-stu-id="9abed-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 




