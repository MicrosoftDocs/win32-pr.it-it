---
description: Apre un archivio certificati specificato.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Store. Open (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327086"
---
# <a name="storeopen-method"></a><span data-ttu-id="0edc8-103">Store. Open (metodo)</span><span class="sxs-lookup"><span data-stu-id="0edc8-103">Store.Open method</span></span>

<span data-ttu-id="0edc8-104">\[Il metodo **Open** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="0edc8-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0edc8-105">Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0edc8-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0edc8-106">Il metodo **Open** apre un [*archivio certificati*](../secgloss/c-gly.md)specificato.</span><span class="sxs-lookup"><span data-stu-id="0edc8-106">The **Open** method opens a specified [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="0edc8-107">Per impostazione predefinita, il percorso dell' \_ \_ Archivio dell'utente di CAPICOM \_ e l'archivio archivio \_ personale \_ sono aperti come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0edc8-107">By default, the CAPICOM\_CURRENT\_USER\_STORE location and CAPICOM\_MY\_STORE store are opened as read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0edc8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0edc8-108">Syntax</span></span>


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0edc8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0edc8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0edc8-110">*StoreLocation* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0edc8-110">*StoreLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0edc8-111">Valore dell'enumerazione del [ \_ \_ percorso dell'archivio CAPICOM](capicom-store-location.md) che indica il percorso dell'archivio da aprire.</span><span class="sxs-lookup"><span data-stu-id="0edc8-111">A value of the [CAPICOM\_STORE\_LOCATION](capicom-store-location.md) enumeration that indicates the location of the store to be opened.</span></span> <span data-ttu-id="0edc8-112">Il valore predefinito è CAPICOM ( \_ \_ archivio utente corrente) \_ .</span><span class="sxs-lookup"><span data-stu-id="0edc8-112">The default value is CAPICOM\_CURRENT\_USER\_STORE.</span></span> <span data-ttu-id="0edc8-113">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0edc8-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0edc8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0edc8-114">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="0edc8-115">Significato</span><span class="sxs-lookup"><span data-stu-id="0edc8-115">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <span data-ttu-id="0edc8-116"><dt>**\_archivio utenti di Active \_ directory \_ di \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-116"><dt>**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="0edc8-117">L'archivio è un archivio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0edc8-117">The store is an Active Directory store.</span></span> <span data-ttu-id="0edc8-118">Se un archivio Active Directory viene aperto in modalità di lettura/scrittura, non verrà generato alcun errore, ma tutte le modifiche apportate all'archivio non verranno rese permanente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-118">No error will be generated if an Active Directory store is opened as read/write, but any changes to the store will not be persisted.</span></span> <span data-ttu-id="0edc8-119">I certificati non possono essere aggiunti o rimossi dagli archivi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0edc8-119">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <span data-ttu-id="0edc8-120"><dt>**\_ \_ archivio utente corrente CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-120"><dt>**CAPICOM\_CURRENT\_USER\_STORE**</dt></span></span> </dl>                             | <span data-ttu-id="0edc8-121">L'archivio è un archivio utente corrente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-121">The store is a current user store.</span></span> <span data-ttu-id="0edc8-122">Un archivio utente corrente può essere un archivio di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0edc8-122">A current user store may be a read/write store.</span></span> <span data-ttu-id="0edc8-123">In caso contrario, le modifiche apportate al contenuto dell'archivio vengono rese permanente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-123">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <span data-ttu-id="0edc8-124"><dt>**\_Archivio del computer locale \_ CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-124"><dt>**CAPICOM\_LOCAL\_MACHINE\_STORE**</dt></span></span> </dl>                          | <span data-ttu-id="0edc8-125">L'archivio è un archivio del computer locale.</span><span class="sxs-lookup"><span data-stu-id="0edc8-125">The store is a local computer store.</span></span> <span data-ttu-id="0edc8-126">Gli archivi del computer locale possono essere archivi di lettura/scrittura solo se l'utente dispone di autorizzazioni di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0edc8-126">Local computer stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="0edc8-127">Se l'utente dispone di autorizzazioni di lettura/scrittura e se l'archivio è aperto in lettura/scrittura, le modifiche apportate al contenuto dell'archivio vengono rese permanente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-127">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <span data-ttu-id="0edc8-128"><dt>**\_Archivio di memoria CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-128"><dt>**CAPICOM\_MEMORY\_STORE**</dt></span></span> </dl>                                                | <span data-ttu-id="0edc8-129">L'archivio è un archivio di memoria.</span><span class="sxs-lookup"><span data-stu-id="0edc8-129">The store is a memory store.</span></span> <span data-ttu-id="0edc8-130">Eventuali modifiche apportate al contenuto dell'archivio non vengono rese permanente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-130">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <span data-ttu-id="0edc8-131"><dt>**\_ \_ \_ archivio utenti smart card \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-131"><dt>**CAPICOM\_SMART\_CARD\_USER\_STORE**</dt></span></span> </dl>                   | <span data-ttu-id="0edc8-132">L'archivio è il gruppo di smart card presenti.</span><span class="sxs-lookup"><span data-stu-id="0edc8-132">The store is the group of present smart cards.</span></span> <span data-ttu-id="0edc8-133">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="0edc8-133">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="0edc8-134">*StoreName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0edc8-134">*StoreName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0edc8-135">Stringa che contiene il nome dell'archivio certificati di sistema da aprire.</span><span class="sxs-lookup"><span data-stu-id="0edc8-135">A string that contains the name of the system certificate store to be opened.</span></span> <span data-ttu-id="0edc8-136">Il valore predefinito è CAPICOMe \_ My \_ Store.</span><span class="sxs-lookup"><span data-stu-id="0edc8-136">The default value is CAPICOM\_MY\_STORE.</span></span> <span data-ttu-id="0edc8-137">Se l'archivio viene aperto da uno script Web, il carattere barra rovesciata ( \\ ) non è consentito nel nome.</span><span class="sxs-lookup"><span data-stu-id="0edc8-137">If the store is opened from a web script, the backslash (\\) character is not allowed in the name.</span></span> <span data-ttu-id="0edc8-138">Oltre agli archivi definiti dal sistema, è possibile aprire gli archivi definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-138">In addition to stores defined by the system, user-defined stores can be opened.</span></span>

<span data-ttu-id="0edc8-139">Questo parametro può essere un archivio definito dall'utente o uno degli archivi certificati di sistema seguenti.</span><span class="sxs-lookup"><span data-stu-id="0edc8-139">This parameter can be a user-defined store or one of the following system certificate stores.</span></span>



| <span data-ttu-id="0edc8-140">Valore</span><span class="sxs-lookup"><span data-stu-id="0edc8-140">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="0edc8-141">Significato</span><span class="sxs-lookup"><span data-stu-id="0edc8-141">Meaning</span></span>                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <span data-ttu-id="0edc8-142"><dt>**\_archivio CA CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-142"><dt>**CAPICOM\_CA\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="0edc8-143">Archivio CA.</span><span class="sxs-lookup"><span data-stu-id="0edc8-143">CA store.</span></span> <span data-ttu-id="0edc8-144">Questo archivio viene usato per archiviare i certificati della CA intermedia.</span><span class="sxs-lookup"><span data-stu-id="0edc8-144">This store is used to store intermediate CA certificates.</span></span><br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <span data-ttu-id="0edc8-145"><dt>**\_archivio personale di CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-145"><dt>**CAPICOM\_MY\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="0edc8-146">Archivio personale.</span><span class="sxs-lookup"><span data-stu-id="0edc8-146">My store.</span></span> <span data-ttu-id="0edc8-147">Questo archivio viene usato per i certificati personali di un utente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-147">This store is used for a user's personal certificates.</span></span><br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <span data-ttu-id="0edc8-148"><dt>**\_ \_ Archivio CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-148"><dt>**CAPICOM\_OTHER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="0edc8-149">Archivio Rubrica.</span><span class="sxs-lookup"><span data-stu-id="0edc8-149">AddressBook store.</span></span> <span data-ttu-id="0edc8-150">Questo archivio viene usato per conservare i certificati di altri utenti.</span><span class="sxs-lookup"><span data-stu-id="0edc8-150">This store is used to keep the certificates of others.</span></span><br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <span data-ttu-id="0edc8-151"><dt>**\_archivio radice CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-151"><dt>**CAPICOM\_ROOT\_STORE**</dt></span></span> </dl>    | <span data-ttu-id="0edc8-152">Archivio radice.</span><span class="sxs-lookup"><span data-stu-id="0edc8-152">Root store.</span></span> <span data-ttu-id="0edc8-153">Questo archivio viene usato per archiviare la CA radice e i certificati attendibili autofirmati.</span><span class="sxs-lookup"><span data-stu-id="0edc8-153">This store is used to store the root CA and self-signed, trusted certificates.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0edc8-154">*OpenMode* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0edc8-154">*OpenMode* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0edc8-155">Valore dell'enumerazione della [ \_ \_ \_ modalità di apertura dell'archivio CAPICOM](capicom-store-open-mode.md) che indica la modalità di apertura dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="0edc8-155">A value of the [CAPICOM\_STORE\_OPEN\_MODE](capicom-store-open-mode.md) enumeration that indicates the open mode of the store.</span></span> <span data-ttu-id="0edc8-156">Il valore predefinito è capicot \_ Store \_ aperto in \_ sola lettura \_ .</span><span class="sxs-lookup"><span data-stu-id="0edc8-156">The default value is CAPICOM\_STORE\_OPEN\_READ\_ONLY.</span></span> <span data-ttu-id="0edc8-157">Se l'archivio viene aperto da uno script Web, questo valore è forzato nell'archivio capicoy \_ \_ aperto \_ \_ solo esistente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-157">If the store is opened from a web script, this value is forced to CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY.</span></span> <span data-ttu-id="0edc8-158">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0edc8-158">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0edc8-159">Valore</span><span class="sxs-lookup"><span data-stu-id="0edc8-159">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="0edc8-160">Significato</span><span class="sxs-lookup"><span data-stu-id="0edc8-160">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <span data-ttu-id="0edc8-161"><dt>**\_ \_ \_ massimo \_ consentito per l'archivio CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-161"><dt>**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</dt></span></span> </dl> | <span data-ttu-id="0edc8-162">Aprire l'archivio in modalità di lettura/scrittura se l'utente dispone di autorizzazioni di lettura/scrittura; in caso contrario, aprire l'archivio in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0edc8-162">Open the store in read/write mode if the user has read/write permissions; otherwise, open the store in read-only mode.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <span data-ttu-id="0edc8-163"><dt>**\_Archivio CAPICOM aperto in \_ \_ sola lettura \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-163"><dt>**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</dt></span></span> </dl>                   | <span data-ttu-id="0edc8-164">Aprire l'archivio in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0edc8-164">Open the store in read-only mode.</span></span><br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <span data-ttu-id="0edc8-165"><dt>**\_Archivio CAPICOM \_ aperto lettura/ \_ \_ scrittura**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-165"><dt>**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</dt></span></span> </dl>                | <span data-ttu-id="0edc8-166">Aprire l'archivio in modalità di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0edc8-166">Open the store in read/write mode.</span></span><br/>                                                                                     |



 

<span data-ttu-id="0edc8-167">I flag seguenti possono essere combinati con i valori della tabella precedente tramite **un'operazione or** logica.</span><span class="sxs-lookup"><span data-stu-id="0edc8-167">The following flags can be combined with the values in the previous table by using a logical-**OR** operation.</span></span>



| <span data-ttu-id="0edc8-168">Valore</span><span class="sxs-lookup"><span data-stu-id="0edc8-168">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="0edc8-169">Significato</span><span class="sxs-lookup"><span data-stu-id="0edc8-169">Meaning</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <span data-ttu-id="0edc8-170"><dt>**\_Archivio CAPICOM \_ aperto \_ \_ solo esistente**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-170"><dt>**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</dt></span></span> </dl>          | <span data-ttu-id="0edc8-171">Apri solo archivi esistenti; non creare un nuovo archivio.</span><span class="sxs-lookup"><span data-stu-id="0edc8-171">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="0edc8-172">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="0edc8-172">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <span data-ttu-id="0edc8-173"><dt>**\_ \_ Archivio CAPICOM aperto \_ include \_ archiviato**</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-173"><dt>**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</dt></span></span> </dl> | <span data-ttu-id="0edc8-174">Includere i certificati archiviati quando si usa l'archivio.</span><span class="sxs-lookup"><span data-stu-id="0edc8-174">Include archived certificates when using the store.</span></span> <span data-ttu-id="0edc8-175">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="0edc8-175">Introduced in CAPICOM 2.0.</span></span><br/>   |



 

<span data-ttu-id="0edc8-176">Gli archivi in alcune posizioni possono essere aperti solo in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0edc8-176">Stores in some locations can be opened only in read-only mode.</span></span> <span data-ttu-id="0edc8-177">Sono inclusi tutti i punti vendita nell'archivio del computer locale capicol \_ \_ \_ per cui l'utente non dispone delle autorizzazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="0edc8-177">These include all stores in CAPICOM\_LOCAL\_MACHINE\_STORE for which the user does not have write permissions.</span></span> <span data-ttu-id="0edc8-178">Tenta di aprire un archivio come archivio di lettura/scrittura senza l'accesso e le autorizzazioni appropriate comporteranno l'errore del metodo **Open** .</span><span class="sxs-lookup"><span data-stu-id="0edc8-178">Attempts to open a store as a read/write store without proper access and permissions will result in the failure of the **Open** method.</span></span> <span data-ttu-id="0edc8-179">Gli archivi di Active Directory possono essere aperti come archivio di lettura/scrittura senza errori del metodo **Open** , ma le modifiche apportate all'archivio non verranno rese permanente.</span><span class="sxs-lookup"><span data-stu-id="0edc8-179">Active Directory stores can be opened as a read/write store without failure of the **Open** method, but changes to the store will not be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0edc8-180">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0edc8-180">Return value</span></span>

<span data-ttu-id="0edc8-181">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0edc8-181">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0edc8-182">Commenti</span><span class="sxs-lookup"><span data-stu-id="0edc8-182">Remarks</span></span>

<span data-ttu-id="0edc8-183">Se questo metodo viene chiamato in un archivio Smart Card, è possibile che vengano richiamate interfacce utente aggiuntive per la smart card.</span><span class="sxs-lookup"><span data-stu-id="0edc8-183">If this method is called on a SmartCard store, additional SmartCard user interfaces may be invoked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0edc8-184">Quando questo metodo viene chiamato da uno script Web, lo script deve accedere ai certificati digitali sul computer locale.</span><span class="sxs-lookup"><span data-stu-id="0edc8-184">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="0edc8-185">Se si consente allo script di accedere ai certificati digitali, il sito Web da cui viene eseguito lo script otterrà anche l'accesso a tutte le informazioni personali archiviate nei certificati.</span><span class="sxs-lookup"><span data-stu-id="0edc8-185">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="0edc8-186">La prima volta che questo metodo viene chiamato da un particolare dominio, viene generata una finestra di dialogo in cui l'utente deve indicare se l'accesso ai certificati deve essere consentito.</span><span class="sxs-lookup"><span data-stu-id="0edc8-186">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span> <span data-ttu-id="0edc8-187">Gli archivi aperti da uno script Web forzano automaticamente il flag capicot \_ Store \_ Open \_ existing \_ .</span><span class="sxs-lookup"><span data-stu-id="0edc8-187">Stores opened from a web script automatically force the CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY flag.</span></span>

 

<span data-ttu-id="0edc8-188">Se *StoreLocation* è l' **\_ \_ \_ \_ archivio utente smart card di capicol**, *StoreName* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0edc8-188">If *StoreLocation* is **CAPICOM\_SMART\_CARD\_USER\_STORE**, *StoreName* is ignored.</span></span> <span data-ttu-id="0edc8-189">In questo caso, CAPICOM legge tutti i certificati da tutti i lettori disponibili che contengono una smart card.</span><span class="sxs-lookup"><span data-stu-id="0edc8-189">In this case, CAPICOM reads all certificates from all available readers that contain a smart card.</span></span>

## <a name="requirements"></a><span data-ttu-id="0edc8-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0edc8-190">Requirements</span></span>



| <span data-ttu-id="0edc8-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edc8-191">Requirement</span></span> | <span data-ttu-id="0edc8-192">Valore</span><span class="sxs-lookup"><span data-stu-id="0edc8-192">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0edc8-193">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0edc8-193">Redistributable</span></span><br/> | <span data-ttu-id="0edc8-194">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="0edc8-194">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0edc8-195">DLL</span><span class="sxs-lookup"><span data-stu-id="0edc8-195">DLL</span></span><br/>             | <dl> <span data-ttu-id="0edc8-196"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0edc8-196"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0edc8-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0edc8-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0edc8-198">**Store**</span><span class="sxs-lookup"><span data-stu-id="0edc8-198">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="0edc8-199">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="0edc8-199">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="0edc8-200">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="0edc8-200">**Close**</span></span>](store-close.md)
</dt> </dl>

 

 
