---
title: parola chiave Union (RPC)
description: Le unioni richiedono parole chiave MIDL speciali per supportarne l'uso con RPC (Remote Procedure Call).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337615"
---
# <a name="union-keyword-rpc"></a><span data-ttu-id="04c85-103">parola chiave Union (RPC)</span><span class="sxs-lookup"><span data-stu-id="04c85-103">union keyword (RPC)</span></span>

<span data-ttu-id="04c85-104">Alcune funzionalità del linguaggio C, ad esempio le unioni, richiedono parole chiave MIDL speciali per supportarne l'utilizzo nelle chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="04c85-104">Some features of the C language, such as unions, require special MIDL keywords to support their use in remote procedure calls.</span></span> <span data-ttu-id="04c85-105">Un'Unione nel linguaggio C è una variabile che include oggetti di dimensioni e tipi diversi.</span><span class="sxs-lookup"><span data-stu-id="04c85-105">A union in the C language is a variable that holds objects of different types and sizes.</span></span> <span data-ttu-id="04c85-106">Lo sviluppatore in genere crea una variabile per tenere traccia dei tipi archiviati nell'Unione.</span><span class="sxs-lookup"><span data-stu-id="04c85-106">The developer usually creates a variable to keep track of the types stored in the union.</span></span> <span data-ttu-id="04c85-107">Per funzionare correttamente in un ambiente distribuito, è necessario che la variabile che indica il tipo di Unione, o *discriminante*, sia disponibile anche per il computer remoto.</span><span class="sxs-lookup"><span data-stu-id="04c85-107">To operate correctly in a distributed environment, the variable that indicates the type of the union, or the *discriminant*, must also be available to the remote computer.</span></span> <span data-ttu-id="04c85-108">MIDL fornisce il \[ [**\_ tipo di Commuter**](/windows/desktop/Midl/switch-type) \] e \[ [**Switch \_ è**](/windows/desktop/Midl/switch-is) \] keywords per identificare il tipo e il nome discriminante.</span><span class="sxs-lookup"><span data-stu-id="04c85-108">MIDL provides the \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] and \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] keywords to identify the discriminant type and name.</span></span>

<span data-ttu-id="04c85-109">MIDL richiede che il discriminante venga trasmesso con l'Unione in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="04c85-109">MIDL requires that the discriminant be transmitted with the union in one of two ways:</span></span>

-   <span data-ttu-id="04c85-110">L'Unione e discriminante devono essere specificati come parametri.</span><span class="sxs-lookup"><span data-stu-id="04c85-110">The union and the discriminant must be provided as parameters.</span></span>
-   <span data-ttu-id="04c85-111">L'Unione e discriminante devono essere inclusi in un pacchetto in una struttura.</span><span class="sxs-lookup"><span data-stu-id="04c85-111">The union and the discriminant must be packaged in a structure.</span></span>

<span data-ttu-id="04c85-112">Due tipi fondamentali di unioni discriminate vengono forniti da MIDL: [**unincapsulated \_**](/windows/desktop/Midl/nonencapsulated-unions) Union e incapsulated [**\_ Union**](/windows/desktop/Midl/encapsulated-unions).</span><span class="sxs-lookup"><span data-stu-id="04c85-112">Two fundamental types of discriminated unions are provided by MIDL: [**nonencapsulated\_union**](/windows/desktop/Midl/nonencapsulated-unions) and [**encapsulated\_union**](/windows/desktop/Midl/encapsulated-unions).</span></span> <span data-ttu-id="04c85-113">Il discriminante di un'Unione non incapsulata è un altro parametro se l'Unione è un parametro.</span><span class="sxs-lookup"><span data-stu-id="04c85-113">The discriminant of a nonencapsulated union is another parameter if the union is a parameter.</span></span> <span data-ttu-id="04c85-114">Si tratta di un altro campo se l'Unione è un campo di una struttura.</span><span class="sxs-lookup"><span data-stu-id="04c85-114">It is another field if the union is a field of a structure.</span></span> <span data-ttu-id="04c85-115">La definizione di un'Unione incapsulata viene trasformata in una definizione di struttura il cui primo campo è discriminante e il cui secondo e l'ultimo campo sono l'Unione.</span><span class="sxs-lookup"><span data-stu-id="04c85-115">The definition of an encapsulated union is turned into a structure definition whose first field is the discriminant and whose second and last fields are the union.</span></span> <span data-ttu-id="04c85-116">Nell'esempio seguente viene illustrato come fornire i parametri Union e discriminante:</span><span class="sxs-lookup"><span data-stu-id="04c85-116">The following example demonstrates how to provide the union and discriminant as parameters:</span></span>

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

<span data-ttu-id="04c85-117">L'Unione nell'esempio precedente può contenere un solo valore, ovvero **short**, **float** o **char**.</span><span class="sxs-lookup"><span data-stu-id="04c85-117">The union in the preceding example can contain a single value: either **short**, **float**, or **char**.</span></span> <span data-ttu-id="04c85-118">La definizione del tipo per l'Unione include l'attributo del **\_ tipo di opzione** MIDL che specifica il tipo di discriminante.</span><span class="sxs-lookup"><span data-stu-id="04c85-118">The type definition for the union includes the MIDL **switch\_type** attribute that specifies the type of the discriminant.</span></span> <span data-ttu-id="04c85-119">Qui, \[ Switch \_ Type (Short) \] specifica che discriminante è di tipo **short**.</span><span class="sxs-lookup"><span data-stu-id="04c85-119">Here, \[switch\_type(short)\] specifies that the discriminant is of type **short**.</span></span> <span data-ttu-id="04c85-120">L'opzione deve essere un tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="04c85-120">The switch must be an integer type.</span></span>

<span data-ttu-id="04c85-121">Se l'Unione è un membro di una struttura, discriminante deve essere un membro della stessa struttura.</span><span class="sxs-lookup"><span data-stu-id="04c85-121">If the union is a member of a structure, then the discriminant must be a member of the same structure.</span></span> <span data-ttu-id="04c85-122">Se l'Unione è un parametro, discriminante deve essere un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="04c85-122">If the union is a parameter, then the discriminant must be another parameter.</span></span> <span data-ttu-id="04c85-123">Il prototipo per la funzione **UnionParamProc** nell'esempio precedente mostra discriminante *sUtype* come ultimo parametro della chiamata.</span><span class="sxs-lookup"><span data-stu-id="04c85-123">The prototype for the function **UnionParamProc** in the preceding example shows the discriminant *sUtype* as the last parameter of the call.</span></span> <span data-ttu-id="04c85-124">(Discriminante può essere visualizzato in qualsiasi posizione nella chiamata). Il tipo del parametro specificato nell' **\[ opzione \_ è \]** l'attributo deve corrispondere al tipo specificato nell'attributo **\[ Switch \_ Type \]** .</span><span class="sxs-lookup"><span data-stu-id="04c85-124">(The discriminant can appear in any position in the call.) The type of the parameter specified in the **\[switch\_is\]** attribute must match the type specified in the **\[switch\_type\]** attribute.</span></span>

<span data-ttu-id="04c85-125">Nell'esempio seguente viene illustrato l'utilizzo di una singola struttura che fornisce il pacchetto di discriminante con l'Unione:</span><span class="sxs-lookup"><span data-stu-id="04c85-125">The following example demonstrates the use of a single structure that packages the discriminant with the union:</span></span>

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

<span data-ttu-id="04c85-126">Il compilatore MIDL Microsoft RPC consente le dichiarazioni Union all'esterno dei costrutti [**typedef**](/windows/desktop/Midl/typedef) .</span><span class="sxs-lookup"><span data-stu-id="04c85-126">The Microsoft RPC MIDL compiler allows union declarations outside of [**typedef**](/windows/desktop/Midl/typedef) constructs.</span></span> <span data-ttu-id="04c85-127">Questa funzionalità è un'estensione di DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="04c85-127">This feature is an extension to DCE IDL.</span></span> <span data-ttu-id="04c85-128">Per ulteriori informazioni, vedere [**Unione**](/windows/desktop/Midl/union).</span><span class="sxs-lookup"><span data-stu-id="04c85-128">For more information, see [**union**](/windows/desktop/Midl/union).</span></span>

 

 