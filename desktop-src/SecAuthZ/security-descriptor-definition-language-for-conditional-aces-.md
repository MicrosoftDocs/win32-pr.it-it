---
description: Una voce di controllo di accesso condizionale (ACE) consente la valutazione di una condizione di accesso quando viene eseguito un controllo di accesso. Il linguaggio SDDL (Security Descriptor Definition Language) fornisce la sintassi per la definizione di Ace condizionali in un formato stringa.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Linguaggio di definizione del descrittore di sicurezza per le voci
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527013"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a><span data-ttu-id="a7d33-104">Linguaggio di definizione del descrittore di sicurezza per le voci</span><span class="sxs-lookup"><span data-stu-id="a7d33-104">Security Descriptor Definition Language for Conditional ACEs</span></span>

<span data-ttu-id="a7d33-105">Una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) condizionale (ACE) consente la valutazione di una condizione di accesso quando viene eseguito un controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="a7d33-105">A conditional [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) allows an access condition to be evaluated when an access check is performed.</span></span> <span data-ttu-id="a7d33-106">Il linguaggio SDDL (Security Descriptor Definition Language) fornisce la sintassi per la definizione di Ace condizionali in un formato stringa.</span><span class="sxs-lookup"><span data-stu-id="a7d33-106">The security descriptor definition language (SDDL) provides syntax for defining conditional ACEs in a string format.</span></span>

<span data-ttu-id="a7d33-107">Il valore SDDL per una voce ACE condizionale è uguale a quello di qualsiasi voce ACE, con la sintassi per l'istruzione condizionale aggiunta alla fine della stringa ACE.</span><span class="sxs-lookup"><span data-stu-id="a7d33-107">The SDDL for a conditional ACE is the same as for any ACE, with the syntax for the conditional statement appended to the end of the ACE string.</span></span> <span data-ttu-id="a7d33-108">Per informazioni su SDDL, vedere [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="a7d33-108">For information about SDDL, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

<span data-ttu-id="a7d33-109">Il \# segno "" è sinonimo di "0" negli attributi delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a7d33-109">The "\#" sign is synonymous with "0" in resource attributes.</span></span> <span data-ttu-id="a7d33-110">Ad esempio, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) equivale a e interpretato come D:ai (XA; OICI; fa;;; WD; (OctetStringType = = \# 01020300)).</span><span class="sxs-lookup"><span data-stu-id="a7d33-110">For example, D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#1\#2\#3\#\#)) is equivalent to and interpreted as D:AI(XA;OICI;FA;;;WD;(OctetStringType==\#01020300)).</span></span>

-   [<span data-ttu-id="a7d33-111">Formato stringa ACE condizionale</span><span class="sxs-lookup"><span data-stu-id="a7d33-111">Conditional ACE String Format</span></span>](#conditional-ace-string-format)
-   [<span data-ttu-id="a7d33-112">Espressioni condizionali</span><span class="sxs-lookup"><span data-stu-id="a7d33-112">Conditional Expressions</span></span>](#conditional-expressions)
-   [<span data-ttu-id="a7d33-113">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="a7d33-113">Attributes</span></span>](#attributes)
-   [<span data-ttu-id="a7d33-114">Operatori</span><span class="sxs-lookup"><span data-stu-id="a7d33-114">Operators</span></span>](#operators)
-   [<span data-ttu-id="a7d33-115">Ordine di precedenza degli operatori</span><span class="sxs-lookup"><span data-stu-id="a7d33-115">Operator Precedence</span></span>](#operator-precedence)
-   [<span data-ttu-id="a7d33-116">Valori sconosciuti</span><span class="sxs-lookup"><span data-stu-id="a7d33-116">Unknown Values</span></span>](#unknown-values)
-   [<span data-ttu-id="a7d33-117">Valutazione ACE condizionale</span><span class="sxs-lookup"><span data-stu-id="a7d33-117">Conditional ACE Evaluation</span></span>](#conditional-ace-evaluation)
-   [<span data-ttu-id="a7d33-118">esempi</span><span class="sxs-lookup"><span data-stu-id="a7d33-118">Examples</span></span>](#examples)
-   [<span data-ttu-id="a7d33-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7d33-119">Related topics</span></span>](#related-topics)

## <a name="conditional-ace-string-format"></a><span data-ttu-id="a7d33-120">Formato stringa ACE condizionale</span><span class="sxs-lookup"><span data-stu-id="a7d33-120">Conditional ACE String Format</span></span>

<span data-ttu-id="a7d33-121">Ogni voce ACE in una stringa del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) è racchiusa tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="a7d33-121">Each ACE in a [*security descriptor*](/windows/desktop/SecGloss/s-gly) string is enclosed in parentheses.</span></span> <span data-ttu-id="a7d33-122">I campi della voce ACE sono nell'ordine seguente e sono separati da punti e virgola (;).</span><span class="sxs-lookup"><span data-stu-id="a7d33-122">The fields of the ACE are in the following order and are separated by semicolons (;).</span></span>

<span data-ttu-id="a7d33-123">*AceType ***;** _AceFlags_* _;_ *_Diritti_*_;_ *_ObjectGUID_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*</span><span class="sxs-lookup"><span data-stu-id="a7d33-123">*AceType\***;**_AceFlags_*_;_*_Rights_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_;(_*_ConditionalExpression_*_)_\*</span></span>

<span data-ttu-id="a7d33-124">I campi sono descritti in [stringhe ACE](ace-strings.md), con le eccezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7d33-124">The fields are as described in [ACE Strings](ace-strings.md), with the following exceptions.</span></span>

-   <span data-ttu-id="a7d33-125">Il campo *AceType* può essere una delle stringhe seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7d33-125">The *AceType* field can be one of the following strings.</span></span>

    | <span data-ttu-id="a7d33-126">Stringa di tipo ACE</span><span class="sxs-lookup"><span data-stu-id="a7d33-126">ACE type string</span></span> | <span data-ttu-id="a7d33-127">Costante in SDDL. h</span><span class="sxs-lookup"><span data-stu-id="a7d33-127">Constant in Sddl.h</span></span>                         | <span data-ttu-id="a7d33-128">Valore AceType</span><span class="sxs-lookup"><span data-stu-id="a7d33-128">AceType value</span></span>                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | <span data-ttu-id="a7d33-129">XA</span><span class="sxs-lookup"><span data-stu-id="a7d33-129">"XA"</span></span><br/> | <span data-ttu-id="a7d33-130">\_accesso callback \_ SDDL \_ consentito</span><span class="sxs-lookup"><span data-stu-id="a7d33-130">SDDL\_CALLBACK\_ACCESS\_ALLOWED</span></span><br/> | <span data-ttu-id="a7d33-131">\_ \_ tipo ACE di callback consentito \_ per \_ l'accesso</span><span class="sxs-lookup"><span data-stu-id="a7d33-131">ACCESS\_ALLOWED\_CALLBACK\_ACE\_TYPE</span></span><br/> |
    | <span data-ttu-id="a7d33-132">XD</span><span class="sxs-lookup"><span data-stu-id="a7d33-132">"XD"</span></span><br/> | <span data-ttu-id="a7d33-133">\_accesso callback \_ SDDL \_ negato</span><span class="sxs-lookup"><span data-stu-id="a7d33-133">SDDL\_CALLBACK\_ACCESS\_DENIED</span></span><br/>  | <span data-ttu-id="a7d33-134">\_ \_ tipo ACE di callback accesso negato \_ \_</span><span class="sxs-lookup"><span data-stu-id="a7d33-134">ACCESS\_DENIED\_CALLBACK\_ACE\_TYPE</span></span><br/>  |

    

     

-   <span data-ttu-id="a7d33-135">Nella stringa ACE sono incluse una o più espressioni condizionali, racchiuse tra parentesi alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="a7d33-135">The ACE string includes one or more conditional expressions, enclosed in parentheses at the end of the string.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="a7d33-136">Espressioni condizionali</span><span class="sxs-lookup"><span data-stu-id="a7d33-136">Conditional Expressions</span></span>

<span data-ttu-id="a7d33-137">Un'espressione condizionale può includere uno qualsiasi degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7d33-137">A conditional expression can include any of the following elements.</span></span>



| <span data-ttu-id="a7d33-138">Elemento dell'espressione</span><span class="sxs-lookup"><span data-stu-id="a7d33-138">Expression element</span></span>                                                | <span data-ttu-id="a7d33-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7d33-139">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d33-140">*AttributeName*</span><span class="sxs-lookup"><span data-stu-id="a7d33-140">*AttributeName*</span></span><br/>                                        | <span data-ttu-id="a7d33-141">Verifica se l'attributo specificato ha un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a7d33-141">Tests whether the specified attribute has a nonzero value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a7d33-142">**Exists** *attributeName*</span><span class="sxs-lookup"><span data-stu-id="a7d33-142">**exists** *AttributeName*</span></span><br/>                             | <span data-ttu-id="a7d33-143">Verifica se l'attributo specificato esiste nel contesto client.</span><span class="sxs-lookup"><span data-stu-id="a7d33-143">Tests whether the specified attribute exists in the client context.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a7d33-144">*Valore* dell' *operatore* *attributeName*</span><span class="sxs-lookup"><span data-stu-id="a7d33-144">*AttributeName* *Operator* *Value*</span></span><br/>                     | <span data-ttu-id="a7d33-145">Restituisce il risultato dell'operazione specificata.</span><span class="sxs-lookup"><span data-stu-id="a7d33-145">Returns the result of the specified operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a7d33-146">\* ConditionalExpression \* **\|\|** _ConditionalExpression_</span><span class="sxs-lookup"><span data-stu-id="a7d33-146">\*ConditionalExpression\***\|\|**_ConditionalExpression_</span></span><br/> | <span data-ttu-id="a7d33-147">Verifica se una delle espressioni condizionali specificate è true.</span><span class="sxs-lookup"><span data-stu-id="a7d33-147">Tests whether either of the specified conditional expressions is true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a7d33-148">*ConditionalExpression* **&&** *ConditionalExpression*</span><span class="sxs-lookup"><span data-stu-id="a7d33-148">*ConditionalExpression* **&&** *ConditionalExpression*</span></span><br/> | <span data-ttu-id="a7d33-149">Verifica se entrambe le espressioni condizionali specificate sono true.</span><span class="sxs-lookup"><span data-stu-id="a7d33-149">Tests whether both of the specified conditional expressions are true.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a7d33-150">**! (**_ConditionalExpression_*_)_*</span><span class="sxs-lookup"><span data-stu-id="a7d33-150">**!(**_ConditionalExpression_*_)_*</span></span><br/>                     | <span data-ttu-id="a7d33-151">Inverso di un'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-151">The inverse of a conditional expression.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a7d33-152">**Membro \_ di {**_SidArray_*_}_*</span><span class="sxs-lookup"><span data-stu-id="a7d33-152">**Member\_of{**_SidArray_*_}_*</span></span><br/>                         | <span data-ttu-id="a7d33-153">Verifica se la matrice di [**SID \_ e \_ attributi**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) del contesto client contiene tutti gli [ID di sicurezza](security-identifiers.md) (SID) nell'elenco delimitato da virgole specificato da *SidArray*.</span><span class="sxs-lookup"><span data-stu-id="a7d33-153">Tests whether the [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) array of the client context contains all of the [Security Identifiers](security-identifiers.md) (SIDs) in the comma-separated list specified by *SidArray*.</span></span><br/> <span data-ttu-id="a7d33-154">Per le voci ACE Consenti, un SID del contesto client deve avere l'attributo **\_ \_ Enabled del gruppo se** impostato per essere considerato una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="a7d33-154">For Allow ACEs, a client context SID must have the **SE\_GROUP\_ENABLED** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="a7d33-155">Per le voci ACE di negazione, un SID del contesto client deve avere il **\_ gruppo se \_ abilitato** oppure il **\_ gruppo se usa solo l'attributo \_ \_ \_ Deny \_ solo per** essere considerato corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a7d33-155">For Deny ACEs, a client context SID must have either the **SE\_GROUP\_ENABLED** or the **SE\_GROUP\_USE\_FOR\_DENY\_ONLY** attribute set to be considered a match.</span></span><br/> <span data-ttu-id="a7d33-156">La matrice *SidArray* può contenere stringhe SID (ad esempio, "S-1-5-6") o alias SID (ad esempio, "BA"</span><span class="sxs-lookup"><span data-stu-id="a7d33-156">The *SidArray* array can contain either SID strings (for example, "S-1-5-6") or SID aliases (for example, "BA"</span></span><br/> |



 

## <a name="attributes"></a><span data-ttu-id="a7d33-157">Attributi</span><span class="sxs-lookup"><span data-stu-id="a7d33-157">Attributes</span></span>

<span data-ttu-id="a7d33-158">Un attributo rappresenta un elemento nella matrice [**di \_ \_ \_ informazioni sugli attributi di sicurezza AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) nel contesto client.</span><span class="sxs-lookup"><span data-stu-id="a7d33-158">An attribute represents an element in the [**AUTHZ\_SECURITY\_ATTRIBUTES\_INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) array in the client context.</span></span> <span data-ttu-id="a7d33-159">Un nome di attributo può contenere tutti i caratteri alfanumerici e i caratteri ":", "/", "." e " \_ ".</span><span class="sxs-lookup"><span data-stu-id="a7d33-159">An attribute name can contain any alphanumeric characters and any of the characters ":", "/", ".", and "\_".</span></span>

<span data-ttu-id="a7d33-160">Un valore di attributo può essere uno dei seguenti tipi.</span><span class="sxs-lookup"><span data-stu-id="a7d33-160">An attribute value can be any of the following types.</span></span>



| <span data-ttu-id="a7d33-161">Tipo di valore</span><span class="sxs-lookup"><span data-stu-id="a7d33-161">Value type</span></span>         | <span data-ttu-id="a7d33-162">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7d33-162">Description</span></span>                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d33-163">Integer</span><span class="sxs-lookup"><span data-stu-id="a7d33-163">Integer</span></span><br/> | <span data-ttu-id="a7d33-164">Intero a 64 bit nella notazione decimale o esadecimale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-164">A 64-bit integer in either decimal or hexadecimal notation.</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a7d33-165">string</span><span class="sxs-lookup"><span data-stu-id="a7d33-165">String</span></span><br/>  | <span data-ttu-id="a7d33-166">Valore stringa delimitato da virgolette.</span><span class="sxs-lookup"><span data-stu-id="a7d33-166">A string value delimited by quotes.</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="a7d33-167">SID</span><span class="sxs-lookup"><span data-stu-id="a7d33-167">SID</span></span><br/>     | <span data-ttu-id="a7d33-168">SID (S-1-1-0) o SID (BA).</span><span class="sxs-lookup"><span data-stu-id="a7d33-168">SID(S-1-1-0) or SID(BA).</span></span> <span data-ttu-id="a7d33-169">Deve essere in RHS del membro \_ del membro o del \_ dispositivo \_ di.</span><span class="sxs-lookup"><span data-stu-id="a7d33-169">Has to be on RHS of Member\_of or Device\_Member\_of.</span></span><br/>                                                                                                           |
| <span data-ttu-id="a7d33-170">BLOB</span><span class="sxs-lookup"><span data-stu-id="a7d33-170">BLOB</span></span><br/>    | <span data-ttu-id="a7d33-171">\# seguito da numeri esadecimali.</span><span class="sxs-lookup"><span data-stu-id="a7d33-171">\# followed by hexadecimal numbers.</span></span> <span data-ttu-id="a7d33-172">Se la lunghezza dei numeri è dispari, l'oggetto \# viene convertito in 0 per renderlo uniforme.</span><span class="sxs-lookup"><span data-stu-id="a7d33-172">If length of the numbers is odd, then the \# is translated to a 0 to make it even.</span></span> <span data-ttu-id="a7d33-173">Inoltre, un oggetto \# visualizzato altrove nel valore viene convertito in 0.</span><span class="sxs-lookup"><span data-stu-id="a7d33-173">Also an \# appearing elsewhere in the value is translated to a 0.</span></span><br/> |



 

## <a name="operators"></a><span data-ttu-id="a7d33-174">Operatori</span><span class="sxs-lookup"><span data-stu-id="a7d33-174">Operators</span></span>

<span data-ttu-id="a7d33-175">Gli operatori seguenti sono definiti per l'utilizzo nelle espressioni condizionali per verificare i valori degli attributi.</span><span class="sxs-lookup"><span data-stu-id="a7d33-175">The following operators are defined for use in conditional expressions to test the values of attributes.</span></span> <span data-ttu-id="a7d33-176">Tutti questi sono operatori binari e usati nel *valore* dell' *operatore* form *attributeName* .</span><span class="sxs-lookup"><span data-stu-id="a7d33-176">All of these are binary operators and used in the form *AttributeName* *Operator* *Value*.</span></span>



| <span data-ttu-id="a7d33-177">Operatore</span><span class="sxs-lookup"><span data-stu-id="a7d33-177">Operator</span></span>            | <span data-ttu-id="a7d33-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7d33-178">Description</span></span>                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | <span data-ttu-id="a7d33-179">Definizione convenzionale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-179">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="a7d33-180">!=</span><span class="sxs-lookup"><span data-stu-id="a7d33-180">!=</span></span><br/>       | <span data-ttu-id="a7d33-181">Definizione convenzionale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-181">Conventional definition.</span></span><br/>                                                                                      |
| <<br/>     | <span data-ttu-id="a7d33-182">Definizione convenzionale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-182">Conventional definition.</span></span><br/>                                                                                      |
| <=<br/>    | <span data-ttu-id="a7d33-183">Definizione convenzionale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-183">Conventional definition.</span></span><br/>                                                                                      |
| ><br/>     | <span data-ttu-id="a7d33-184">Definizione convenzionale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-184">Conventional definition.</span></span><br/>                                                                                      |
| >=<br/>    | <span data-ttu-id="a7d33-185">Definizione convenzionale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-185">Conventional definition.</span></span><br/>                                                                                      |
| <span data-ttu-id="a7d33-186">Contiene</span><span class="sxs-lookup"><span data-stu-id="a7d33-186">Contains</span></span><br/> | <span data-ttu-id="a7d33-187">**True** se il valore dell'attributo specificato è un superset del valore specificato. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a7d33-187">**TRUE** if the value of the specified attribute is a superset of the specified value; otherwise, **FALSE**.</span></span><br/>  |
| <span data-ttu-id="a7d33-188">Qualsiasi \_</span><span class="sxs-lookup"><span data-stu-id="a7d33-188">Any\_of</span></span><br/>  | <span data-ttu-id="a7d33-189">**True** se il valore specificato è un superset del valore dell'attributo specificato. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a7d33-189">**TRUE** if the specified value is a superset of the value of the specified attribute; otherwise, **FALSE**.</span></span> <br/> |



 

<span data-ttu-id="a7d33-190">Inoltre, gli operatori unari esistono, il membro \_ di e la negazione (!) sono definiti come descritto nella tabella espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="a7d33-190">In addition, the unary operators Exists, Member\_of, and negation (!) are defined as described in the Conditional Expressions table.</span></span>

<span data-ttu-id="a7d33-191">L'operatore "Contains" deve essere preceduto e seguito da uno spazio vuoto e l'operatore "Any \_ of" deve essere preceduto da uno spazio vuoto.</span><span class="sxs-lookup"><span data-stu-id="a7d33-191">The "Contains" operator must be preceded and followed by white space, and the "Any\_of" operator must be preceded by white space.</span></span>

## <a name="operator-precedence"></a><span data-ttu-id="a7d33-192">Ordine di precedenza degli operatori</span><span class="sxs-lookup"><span data-stu-id="a7d33-192">Operator Precedence</span></span>

<span data-ttu-id="a7d33-193">Gli operatori vengono valutati nell'ordine di precedenza seguente, in cui le operazioni di uguale precedenza vengono valutate da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="a7d33-193">The operators are evaluated in the following order of precedence, with operations of equal precedence being evaluated from left to right.</span></span>

1.  <span data-ttu-id="a7d33-194">Exists, membro \_ di</span><span class="sxs-lookup"><span data-stu-id="a7d33-194">Exists, Member\_of</span></span>
2.  <span data-ttu-id="a7d33-195">Contiene \_ , qualsiasi</span><span class="sxs-lookup"><span data-stu-id="a7d33-195">Contains, Any\_of</span></span>
3.  <span data-ttu-id="a7d33-196">= =,! =, <, <=, >, >=</span><span class="sxs-lookup"><span data-stu-id="a7d33-196">==, !=, <, <=, >, >=</span></span>
4.  <span data-ttu-id="a7d33-197">!</span><span class="sxs-lookup"><span data-stu-id="a7d33-197">!</span></span>
5.  &&
6.  \|\|

<span data-ttu-id="a7d33-198">Inoltre, qualsiasi parte di un'espressione condizionale può essere racchiusa tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="a7d33-198">In addition, any portion of a conditional expression can be enclosed in parenthesis.</span></span> <span data-ttu-id="a7d33-199">Le espressioni racchiuse tra parentesi vengono valutate per prime.</span><span class="sxs-lookup"><span data-stu-id="a7d33-199">Expressions within parentheses are evaluated first.</span></span>

## <a name="unknown-values"></a><span data-ttu-id="a7d33-200">Valori sconosciuti</span><span class="sxs-lookup"><span data-stu-id="a7d33-200">Unknown Values</span></span>

<span data-ttu-id="a7d33-201">I risultati delle espressioni condizionali restituiscono talvolta un valore **sconosciuto**.</span><span class="sxs-lookup"><span data-stu-id="a7d33-201">The results of conditional expressions sometimes return a value of **Unknown**.</span></span> <span data-ttu-id="a7d33-202">Ad esempio, una qualsiasi delle operazioni relazionali restituisce **Unknown** quando l'attributo specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="a7d33-202">For example, any of the relational operations return **Unknown** when the specified attribute does not exist.</span></span>

<span data-ttu-id="a7d33-203">Nella tabella seguente vengono descritti i risultati di un'operazione **and** logica tra due espressioni condizionali, *ConditionalExpression1* e *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="a7d33-203">The following table describes the results for a logical **AND** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="a7d33-204">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="a7d33-204">*ConditionalExpression1*</span></span> | <span data-ttu-id="a7d33-205">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="a7d33-205">*ConditionalExpression2*</span></span> | <span data-ttu-id="a7d33-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="a7d33-206">*ConditionalExpression1* **&&** *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|----------------------------------------------------------|
| <span data-ttu-id="a7d33-207">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-207">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-208">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-208">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-209">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-209">**TRUE**</span></span><br/>                                      |
| <span data-ttu-id="a7d33-210">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-210">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-211">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-211">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-212">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-212">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="a7d33-213">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-213">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-214">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-214">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-215">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-215">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="a7d33-216">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-216">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-217">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-217">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-218">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-218">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="a7d33-219">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-219">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-220">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-220">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-221">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-221">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="a7d33-222">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-222">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-223">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-223">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-224">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-224">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="a7d33-225">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-225">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-226">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-226">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-227">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-227">**UNKNOWN**</span></span><br/>                                   |
| <span data-ttu-id="a7d33-228">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-228">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-229">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-229">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-230">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-230">**FALSE**</span></span><br/>                                     |
| <span data-ttu-id="a7d33-231">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-231">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-232">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-232">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-233">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-233">**UNKNOWN**</span></span><br/>                                   |



 

<span data-ttu-id="a7d33-234">Nella tabella seguente vengono descritti i risultati di un'operazione **or** logica tra due espressioni condizionali, *ConditionalExpression1* e *ConditionalExpression2*.</span><span class="sxs-lookup"><span data-stu-id="a7d33-234">The following table describes the results for a logical **OR** operation between two conditional expressions, *ConditionalExpression1* and *ConditionalExpression2*.</span></span>



| <span data-ttu-id="a7d33-235">*ConditionalExpression1*</span><span class="sxs-lookup"><span data-stu-id="a7d33-235">*ConditionalExpression1*</span></span> | <span data-ttu-id="a7d33-236">*ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="a7d33-236">*ConditionalExpression2*</span></span> | <span data-ttu-id="a7d33-237">*ConditionalExpression1* \*\*</span><span class="sxs-lookup"><span data-stu-id="a7d33-237">*ConditionalExpression1* \*\*</span></span>\|\|<span data-ttu-id="a7d33-238">\*\* *ConditionalExpression2*</span><span class="sxs-lookup"><span data-stu-id="a7d33-238">\*\* *ConditionalExpression2*</span></span> |
|--------------------------|--------------------------|------------------------------------------------------------|
| <span data-ttu-id="a7d33-239">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-239">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-240">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-240">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-241">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-241">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="a7d33-242">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-242">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-243">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-243">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-244">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-244">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="a7d33-245">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-245">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-246">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-246">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-247">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-247">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="a7d33-248">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-248">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-249">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-249">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-250">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-250">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="a7d33-251">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-251">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-252">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-252">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-253">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-253">**FALSE**</span></span><br/>                                       |
| <span data-ttu-id="a7d33-254">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-254">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-255">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-255">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-256">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-256">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="a7d33-257">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-257">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-258">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-258">**TRUE**</span></span><br/>      | <span data-ttu-id="a7d33-259">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-259">**TRUE**</span></span><br/>                                        |
| <span data-ttu-id="a7d33-260">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-260">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-261">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a7d33-261">**FALSE**</span></span><br/>     | <span data-ttu-id="a7d33-262">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-262">**UNKNOWN**</span></span><br/>                                     |
| <span data-ttu-id="a7d33-263">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-263">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-264">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-264">**UNKNOWN**</span></span><br/>   | <span data-ttu-id="a7d33-265">**UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="a7d33-265">**UNKNOWN**</span></span><br/>                                     |



 

<span data-ttu-id="a7d33-266">Anche la negazione di un'espressione condizionale con un valore **sconosciuto** è **sconosciuta**.</span><span class="sxs-lookup"><span data-stu-id="a7d33-266">The negation of a conditional expression with a value of **UNKNOWN** is also **UNKNOWN**.</span></span>

## <a name="conditional-ace-evaluation"></a><span data-ttu-id="a7d33-267">Valutazione ACE condizionale</span><span class="sxs-lookup"><span data-stu-id="a7d33-267">Conditional ACE Evaluation</span></span>

<span data-ttu-id="a7d33-268">La tabella seguente descrive il risultato del controllo di accesso di una voce ACE condizionale a seconda della valutazione finale dell'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="a7d33-268">The following table describes the access check result of a conditional ACE depending on the final evaluation of the conditional expression.</span></span>

| <span data-ttu-id="a7d33-269">Tipo ACE</span><span class="sxs-lookup"><span data-stu-id="a7d33-269">ACE type</span></span>         | <span data-ttu-id="a7d33-270">true</span><span class="sxs-lookup"><span data-stu-id="a7d33-270">TRUE</span></span>             | <span data-ttu-id="a7d33-271">FALSE</span><span class="sxs-lookup"><span data-stu-id="a7d33-271">FALSE</span></span>                 | <span data-ttu-id="a7d33-272">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="a7d33-272">UNKNOWN</span></span>               |
|------------------|------------------|-----------------------|-----------------------|
| <span data-ttu-id="a7d33-273">Allow</span><span class="sxs-lookup"><span data-stu-id="a7d33-273">Allow</span></span><br/> | <span data-ttu-id="a7d33-274">Allow</span><span class="sxs-lookup"><span data-stu-id="a7d33-274">Allow</span></span><br/> | <span data-ttu-id="a7d33-275">Ignora ACE</span><span class="sxs-lookup"><span data-stu-id="a7d33-275">Ignore ACE</span></span><br/> | <span data-ttu-id="a7d33-276">Ignora ACE</span><span class="sxs-lookup"><span data-stu-id="a7d33-276">Ignore ACE</span></span><br/> |
| <span data-ttu-id="a7d33-277">Nega</span><span class="sxs-lookup"><span data-stu-id="a7d33-277">Deny</span></span><br/>  | <span data-ttu-id="a7d33-278">Nega</span><span class="sxs-lookup"><span data-stu-id="a7d33-278">Deny</span></span><br/>  | <span data-ttu-id="a7d33-279">Ignora ACE</span><span class="sxs-lookup"><span data-stu-id="a7d33-279">Ignore ACE</span></span><br/> | <span data-ttu-id="a7d33-280">Nega</span><span class="sxs-lookup"><span data-stu-id="a7d33-280">Deny</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="a7d33-281">Esempio</span><span class="sxs-lookup"><span data-stu-id="a7d33-281">Examples</span></span>

<span data-ttu-id="a7d33-282">Negli esempi seguenti viene illustrato il modo in cui i criteri di accesso specificati sono rappresentati da una voce ACE condizionale definita mediante SDDL.</span><span class="sxs-lookup"><span data-stu-id="a7d33-282">The following examples show how the specified access policies are represented by a conditional ACE defined by using SDDL.</span></span>

<dl> <dt>

<span data-ttu-id="a7d33-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica</span><span class="sxs-lookup"><span data-stu-id="a7d33-283"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="a7d33-284">Consenti Esegui a tutti se sono soddisfatte entrambe le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7d33-284">Allow Execute to Everyone if both of the following conditions are met:</span></span>

-   <span data-ttu-id="a7d33-285">Titolo = PM</span><span class="sxs-lookup"><span data-stu-id="a7d33-285">Title = PM</span></span>
-   <span data-ttu-id="a7d33-286">Divisione = Finance o Division = Sales</span><span class="sxs-lookup"><span data-stu-id="a7d33-286">Division = Finance or Division = Sales</span></span>

</dd> <dt>

<span data-ttu-id="a7d33-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="a7d33-287"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="a7d33-288">D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Finance" \| \| @User.Division = = "Sales")))</span><span class="sxs-lookup"><span data-stu-id="a7d33-288">D:(XA; ;FX;;;S-1-1-0; (@User.Title=="PM" && (@User.Division=="Finance" \|\| @User.Division ==" Sales")))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="a7d33-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica</span><span class="sxs-lookup"><span data-stu-id="a7d33-289"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="a7d33-290">Consenti Esegui se uno dei progetti utente si interseca con i progetti del file.</span><span class="sxs-lookup"><span data-stu-id="a7d33-290">Allow execute if any of the user s projects intersect with the file s projects.</span></span>

</dd> <dt>

<span data-ttu-id="a7d33-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="a7d33-291"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="a7d33-292">D: (XA;; FX;;; S-1-1-0; ( @User.Project Qualsiasi \_ @Resource.Project ))</span><span class="sxs-lookup"><span data-stu-id="a7d33-292">D:(XA; ;FX;;;S-1-1-0; (@User.Project Any\_of @Resource.Project))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span data-ttu-id="a7d33-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica</span><span class="sxs-lookup"><span data-stu-id="a7d33-293"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy</span></span>
</dt> <dd>

<span data-ttu-id="a7d33-294">Consenti l'accesso in lettura se l'utente ha eseguito l'accesso con una smart card, è un operatore di backup e si connette da un computer con BitLocker abilitato.</span><span class="sxs-lookup"><span data-stu-id="a7d33-294">Allow read access if the user has logged in with a smart card, is a backup operator, and is connecting from a machine with Bitlocker enabled.</span></span>

</dd> <dt>

<span data-ttu-id="a7d33-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span><span class="sxs-lookup"><span data-stu-id="a7d33-295"><span id="SDDL"></span><span id="sddl"></span>SDDL</span></span>
</dt> <dd>

<span data-ttu-id="a7d33-296">D: (XA;; FR;;; S-1-1-0; (Membro \_ di {SID (SID smart card \_ ), SID (BO)}  && @Device.Bitlocker ))</span><span class="sxs-lookup"><span data-stu-id="a7d33-296">D:(XA; ;FR;;;S-1-1-0; (Member\_of {SID(Smartcard\_SID), SID(BO)} && @Device.Bitlocker))</span></span>

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a7d33-297">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7d33-297">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a7d33-298">[\[MS-DTYP \] : Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="a7d33-298">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

