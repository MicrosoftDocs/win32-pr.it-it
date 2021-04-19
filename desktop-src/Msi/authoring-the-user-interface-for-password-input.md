---
description: Per ogni password che deve essere immessa dall'utente, aggiungere un controllo di modifica in una finestra di dialogo in cui è archiviato il valore della password in una proprietà.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Creazione dell'interfaccia utente per l'input della password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311029"
---
# <a name="authoring-the-user-interface-for-password-input"></a><span data-ttu-id="b4dd0-103">Creazione dell'interfaccia utente per l'input della password</span><span class="sxs-lookup"><span data-stu-id="b4dd0-103">Authoring the User Interface for Password Input</span></span>

<span data-ttu-id="b4dd0-104">Per ogni password che deve essere immessa dall'utente, aggiungere un controllo di modifica in una finestra di dialogo in cui è archiviato il valore della password in una proprietà.</span><span class="sxs-lookup"><span data-stu-id="b4dd0-104">For each password that must be entered by the user, add an edit control on a dialog that stores the value of the password into a property.</span></span> <span data-ttu-id="b4dd0-105">Questo [controllo di modifica](edit-control.md) deve avere l' [attributo di controllo password](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="b4dd0-105">This [edit control](edit-control.md) should have the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="b4dd0-106">Specifica che la proprietà immessa è una password e impedisce al programma di installazione di scrivere la proprietà nel file di log.</span><span class="sxs-lookup"><span data-stu-id="b4dd0-106">This specifies that the property entered is a password and prevents the installer from writing the property to the log file.</span></span>

<span data-ttu-id="b4dd0-107">Gli [attributi del controllo](control-attributes.md) per il controllo di modifica della password sono MsidbControlAttributesVisible, MsidbControlAttributesEnabled e msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span><span class="sxs-lookup"><span data-stu-id="b4dd0-107">The [control attributes](control-attributes.md) for the password edit control are msidbControlAttributesVisible, msidbControlAttributesEnabled, and msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span></span> <span data-ttu-id="b4dd0-108">X, Y, larghezza, altezza e controllo \_ dipendono dal layout del controllo nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b4dd0-108">The X, Y, Width, Height, and Control\_Next depend on the layout of the control on the dialog.</span></span>

[<span data-ttu-id="b4dd0-109">Tabella di controllo</span><span class="sxs-lookup"><span data-stu-id="b4dd0-109">Control Table</span></span>](control-table.md)



| <span data-ttu-id="b4dd0-110">Finestra di dialogo\_</span><span class="sxs-lookup"><span data-stu-id="b4dd0-110">Dialog\_</span></span> | <span data-ttu-id="b4dd0-111">controllo\_</span><span class="sxs-lookup"><span data-stu-id="b4dd0-111">Control\_</span></span>            | <span data-ttu-id="b4dd0-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4dd0-112">Type</span></span> | <span data-ttu-id="b4dd0-113">X</span><span class="sxs-lookup"><span data-stu-id="b4dd0-113">X</span></span>   | <span data-ttu-id="b4dd0-114">S</span><span class="sxs-lookup"><span data-stu-id="b4dd0-114">Y</span></span>   | <span data-ttu-id="b4dd0-115">Larghezza</span><span class="sxs-lookup"><span data-stu-id="b4dd0-115">Width</span></span> | <span data-ttu-id="b4dd0-116">Altezza</span><span class="sxs-lookup"><span data-stu-id="b4dd0-116">Height</span></span> | <span data-ttu-id="b4dd0-117">Attributi</span><span class="sxs-lookup"><span data-stu-id="b4dd0-117">Attributes</span></span> | <span data-ttu-id="b4dd0-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4dd0-118">Property</span></span>         | <span data-ttu-id="b4dd0-119">Testo</span><span class="sxs-lookup"><span data-stu-id="b4dd0-119">Text</span></span> | <span data-ttu-id="b4dd0-120">Controllo \_ successivo</span><span class="sxs-lookup"><span data-stu-id="b4dd0-120">Control\_Next</span></span> | <span data-ttu-id="b4dd0-121">Help</span><span class="sxs-lookup"><span data-stu-id="b4dd0-121">Help</span></span> |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| <span data-ttu-id="b4dd0-122">MyDialog</span><span class="sxs-lookup"><span data-stu-id="b4dd0-122">MyDialog</span></span> | <span data-ttu-id="b4dd0-123">TestUserPasswordEdit</span><span class="sxs-lookup"><span data-stu-id="b4dd0-123">TestUserPasswordEdit</span></span> | <span data-ttu-id="b4dd0-124">Modifica</span><span class="sxs-lookup"><span data-stu-id="b4dd0-124">Edit</span></span> | <span data-ttu-id="b4dd0-125">25</span><span class="sxs-lookup"><span data-stu-id="b4dd0-125">25</span></span>  | <span data-ttu-id="b4dd0-126">120</span><span class="sxs-lookup"><span data-stu-id="b4dd0-126">120</span></span> | <span data-ttu-id="b4dd0-127">300</span><span class="sxs-lookup"><span data-stu-id="b4dd0-127">300</span></span>   | <span data-ttu-id="b4dd0-128">20</span><span class="sxs-lookup"><span data-stu-id="b4dd0-128">20</span></span>     | <span data-ttu-id="b4dd0-129">2097155</span><span class="sxs-lookup"><span data-stu-id="b4dd0-129">2097155</span></span>    | <span data-ttu-id="b4dd0-130">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="b4dd0-130">TESTUSERPASSWORD</span></span> |      | <span data-ttu-id="b4dd0-131">Annulla</span><span class="sxs-lookup"><span data-stu-id="b4dd0-131">Cancel</span></span>        |      |



 

<span data-ttu-id="b4dd0-132">Continuare a [proteggere l'installazione](securing-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="b4dd0-132">Continue to [Securing the installation](securing-the-installation.md).</span></span>

 

 



