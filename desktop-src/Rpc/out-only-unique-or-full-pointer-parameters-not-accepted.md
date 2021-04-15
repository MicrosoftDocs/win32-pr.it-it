---
title: Out-Only parametri del puntatore univoco o completo non accettati
description: I puntatori univoci o completi che sono \ out solo non sono accettati dal compilatore MIDL. Tali specifiche fanno sì che il compilatore MIDL generi un messaggio di errore.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516977"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a><span data-ttu-id="92026-104">Out-Only parametri del puntatore univoco o completo non accettati</span><span class="sxs-lookup"><span data-stu-id="92026-104">Out-Only Unique or Full Pointer Parameters Not Accepted</span></span>

<span data-ttu-id="92026-105">I puntatori univoci o completi \[ [](/windows/desktop/Midl/out-idl) \] non sono accettati dal compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="92026-105">Unique or full pointers that are \[ [out](/windows/desktop/Midl/out-idl)\]-only are not accepted by the MIDL compiler.</span></span> <span data-ttu-id="92026-106">Tali specifiche fanno sì che il compilatore MIDL generi un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="92026-106">Such specifications cause the MIDL compiler to generate an error message.</span></span>

<span data-ttu-id="92026-107">Lo stub del server generato automaticamente deve allocare memoria per il referente del puntatore, in modo che l'applicazione server possa archiviare i dati nell'area di memoria.</span><span class="sxs-lookup"><span data-stu-id="92026-107">The automatically generated server stub has to allocate memory for the pointer referent so that the server application can store data in that memory area.</span></span> <span data-ttu-id="92026-108">In base alla definizione di un parametro di sola **\[ uscita \]**, nessuna informazione sul parametro viene trasmessa dal client al server.</span><span class="sxs-lookup"><span data-stu-id="92026-108">According to the definition of an **\[out\]**-only parameter, no information about the parameter is transmitted from client to server.</span></span> <span data-ttu-id="92026-109">Nel caso di un puntatore univoco, che può assumere il valore null, lo stub del server non dispone di informazioni sufficienti per duplicare correttamente il puntatore univoco nello spazio degli indirizzi del server, né lo stub contiene informazioni sul fatto che il puntatore punti a un indirizzo valido o se deve essere impostato su null.</span><span class="sxs-lookup"><span data-stu-id="92026-109">In the case of a unique pointer, which can take the value null, the server stub does not have enough information to correctly duplicate the unique pointer in the server's address space, nor does the stub have any information about whether the pointer should point to a valid address or whether it should be set to null.</span></span> <span data-ttu-id="92026-110">Questa combinazione non è pertanto consentita.</span><span class="sxs-lookup"><span data-stu-id="92026-110">Therefore, this combination is not allowed.</span></span>

<span data-ttu-id="92026-111">Invece di \[ **out**, [Unique](/windows/desktop/Midl/unique) \] o \[ **out**, [](/windows/desktop/Midl/ptr) \] puntatori PTR, utilizzare \[ **in**, **out**, **Unique** \] o \[ **in**, **out**, **ptr** \] puntatori o utilizzare un altro livello di riferimento indiretto, ad esempio un puntatore di riferimento che punta al puntatore univoco o completo valido.</span><span class="sxs-lookup"><span data-stu-id="92026-111">Rather than \[**out**, [unique](/windows/desktop/Midl/unique)\] or \[**out**, [ptr](/windows/desktop/Midl/ptr)\] pointers, use \[**in**, **out**, **unique**\] or \[**in**, **out**, **ptr**\] pointers, or use another level of indirection such as a reference pointer that points to the valid unique or full pointer.</span></span>

 

 