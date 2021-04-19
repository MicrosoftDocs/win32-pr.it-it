---
description: Contiene il percorso del file icona per la connessione.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Elemento ICONFilePath (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307539"
---
# <a name="iconfilepath-mbnprofile-element"></a><span data-ttu-id="d62dd-103">Elemento ICONFilePath (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="d62dd-103">ICONFilePath (MBNProfile) Element</span></span>

<span data-ttu-id="d62dd-104">L'elemento **ICONFilePath (MBNProfile)** contiene il percorso del file icona per la connessione.</span><span class="sxs-lookup"><span data-stu-id="d62dd-104">The **ICONFilePath (MBNProfile)** element contains the path of the icon file for the connection.</span></span>

<span data-ttu-id="d62dd-105">L'interfaccia utente di connessione al sistema operativo visualizzerà questa icona quando si effettua una connessione utilizzando questo elemento.</span><span class="sxs-lookup"><span data-stu-id="d62dd-105">The operating system connection UI will display this icon when a connection is made using this element.</span></span>

<span data-ttu-id="d62dd-106">Quando si passa il codice XML per la creazione del profilo nel metodo [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) dell'interfaccia [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) , questo percorso deve puntare al percorso di origine del file icona.</span><span class="sxs-lookup"><span data-stu-id="d62dd-106">When passing the XML for creating the profile in the [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) method of the [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) interface, this path should point to the source location of the icon file.</span></span> <span data-ttu-id="d62dd-107">Al completamento della creazione dell'oggetto [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) , il servizio Mobile Broadband copia il file dell'icona nell'archivio interno e il percorso del profilo verrà modificato in modo da riflettere questo problema.</span><span class="sxs-lookup"><span data-stu-id="d62dd-107">On successful creation of [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) object, the Mobile Broadband service will copy the icon file in it's internal store and the profile path will be modified to reflect this.</span></span>

<span data-ttu-id="d62dd-108">Il file icona deve essere in formato BMP con la dimensione 32X32 pixel.</span><span class="sxs-lookup"><span data-stu-id="d62dd-108">The icon file should be in .bmp format with 32X32 pixel dimension.</span></span>

<span data-ttu-id="d62dd-109">Questo elemento è una stringa di lunghezza massima di 1024 caratteri, che contiene un percorso di file assoluto.</span><span class="sxs-lookup"><span data-stu-id="d62dd-109">This element is a string of length up to 1024 characters, containing an absolute file path.</span></span>

<span data-ttu-id="d62dd-110">L'elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d62dd-110">The element is optional.</span></span>

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

<span data-ttu-id="d62dd-111">L'elemento **ICONFilePath** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d62dd-111">The **ICONFilePath** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d62dd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d62dd-112">Requirements</span></span>



| <span data-ttu-id="d62dd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d62dd-113">Requirement</span></span> | <span data-ttu-id="d62dd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d62dd-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d62dd-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d62dd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d62dd-116">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d62dd-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d62dd-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d62dd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d62dd-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d62dd-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d62dd-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d62dd-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="d62dd-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="d62dd-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d62dd-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d62dd-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="d62dd-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="d62dd-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d62dd-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d62dd-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




