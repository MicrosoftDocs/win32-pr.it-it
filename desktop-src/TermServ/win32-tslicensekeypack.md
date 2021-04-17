---
title: Classe Win32_TSLicenseKeyPack
description: Fornisce metodi e proprietà per la visualizzazione e l'installazione di Servizi Desktop remoto key pack per le licenze.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517403"
---
# <a name="win32_tslicensekeypack-class"></a><span data-ttu-id="b02e3-105">Win32 \_ TSLicenseKeyPack (classe)</span><span class="sxs-lookup"><span data-stu-id="b02e3-105">Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="b02e3-106">Fornisce metodi e proprietà per la visualizzazione e l'installazione di Servizi Desktop remoto key pack per le licenze.</span><span class="sxs-lookup"><span data-stu-id="b02e3-106">Provides methods and properties for viewing and installing Remote Desktop Services license key packs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b02e3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b02e3-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a><span data-ttu-id="b02e3-108">Members</span><span class="sxs-lookup"><span data-stu-id="b02e3-108">Members</span></span>

<span data-ttu-id="b02e3-109">La classe **Win32 \_ TSLicenseKeyPack** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b02e3-109">The **Win32\_TSLicenseKeyPack** class has these types of members:</span></span>

-   [<span data-ttu-id="b02e3-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="b02e3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b02e3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b02e3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b02e3-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b02e3-112">Methods</span></span>

<span data-ttu-id="b02e3-113">La classe **Win32 \_ TSLicenseKeyPack** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b02e3-113">The **Win32\_TSLicenseKeyPack** class has these methods.</span></span>



| <span data-ttu-id="b02e3-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="b02e3-114">Method</span></span>                                                                                                        | <span data-ttu-id="b02e3-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b02e3-115">Description</span></span>                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b02e3-116">**ConvertLicenses**</span><span class="sxs-lookup"><span data-stu-id="b02e3-116">**ConvertLicenses**</span></span>](convertlicenses-win32-tslicensekeypack.md)                                             | <span data-ttu-id="b02e3-117">Converte le licenze nel Key Pack corrente.</span><span class="sxs-lookup"><span data-stu-id="b02e3-117">Converts the licenses in the current key pack.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="b02e3-118">**ImportAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-118">**ImportAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | <span data-ttu-id="b02e3-119">Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="b02e3-119">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/> |
| [<span data-ttu-id="b02e3-120">**ImportLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="b02e3-120">**ImportLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | <span data-ttu-id="b02e3-121">Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License che usa un identificatore di licenza ricevuto tramite Internet o il telefono.</span><span class="sxs-lookup"><span data-stu-id="b02e3-121">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span><br/>                                               |
| [<span data-ttu-id="b02e3-122">**ImportOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-122">**ImportOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | <span data-ttu-id="b02e3-123">Importazioni, da un altro Desktop remoto server licenze, un Key Pack per licenze Open License Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b02e3-123">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="b02e3-124">**ImportRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-124">**ImportRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | <span data-ttu-id="b02e3-125">Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="b02e3-125">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                   |
| [<span data-ttu-id="b02e3-126">**InstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-126">**InstallAgreementLicenseKeyPack**</span></span>](installagreementlicensekeypack-win32-tslicensekeypack.md)               | <span data-ttu-id="b02e3-127">Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite una licenza per il contratto.</span><span class="sxs-lookup"><span data-stu-id="b02e3-127">Installs a Remote Desktop Services license key pack that was purchased through an agreement license.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="b02e3-128">**InstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-128">**InstallLicenseKeyPack**</span></span>](installlicensekeypack-win32-tslicensekeypack.md)                                 | <span data-ttu-id="b02e3-129">Installa un Key Pack per le licenze Servizi Desktop remoto che usa un ID del Key Pack per le licenze ricevuto tramite Internet o il telefono.</span><span class="sxs-lookup"><span data-stu-id="b02e3-129">Installs a Remote Desktop Services license key pack that uses a license key pack ID that was received over the Internet or the phone.</span></span><br/>                                                                                          |
| [<span data-ttu-id="b02e3-130">**InstallOpenLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-130">**InstallOpenLicenseKeyPack**</span></span>](installopenlicensekeypack-win32-tslicensekeypack.md)                         | <span data-ttu-id="b02e3-131">Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza Open.</span><span class="sxs-lookup"><span data-stu-id="b02e3-131">Installs a Remote Desktop Services license key pack that was purchased through an open license agreement.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="b02e3-132">**InstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-132">**InstallRetailPurchaseLicenseKeyPack**</span></span>](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | <span data-ttu-id="b02e3-133">Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un negozio al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="b02e3-133">Installs a Remote Desktop Services license key pack that was purchased through a retail store.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="b02e3-134">**ReinstallAgreementLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-134">**ReinstallAgreementLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | <span data-ttu-id="b02e3-135">Reinstalla un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="b02e3-135">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span><br/>                                           |
| [<span data-ttu-id="b02e3-136">**ReinstallLicenseKeyPackOffline**</span><span class="sxs-lookup"><span data-stu-id="b02e3-136">**ReinstallLicenseKeyPackOffline**</span></span>](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | <span data-ttu-id="b02e3-137">Reinstalla un Key Pack di Servizi Desktop remoto License che utilizza l'identificatore di licenza ricevuto tramite Internet o il telefono.</span><span class="sxs-lookup"><span data-stu-id="b02e3-137">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span><br/>                                                                                       |
| [<span data-ttu-id="b02e3-138">**ReinstallOpenPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-138">**ReinstallOpenPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | <span data-ttu-id="b02e3-139">Reinstalla un Key Pack per licenze Open License Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b02e3-139">Reinstalls an Open License Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="b02e3-140">**ReinstallRetailPurchaseLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-140">**ReinstallRetailPurchaseLicenseKeyPack**</span></span>](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | <span data-ttu-id="b02e3-141">Reinstalla un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="b02e3-141">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="b02e3-142">**RemoveLicensesWithIdCount**</span><span class="sxs-lookup"><span data-stu-id="b02e3-142">**RemoveLicensesWithIdCount**</span></span>](win32-tslicensekeypack-removelicenseswithidcount.md)                         | <span data-ttu-id="b02e3-143">Rimuove il numero specificato di Servizi Desktop remoto licenze dal Key Pack specificato.</span><span class="sxs-lookup"><span data-stu-id="b02e3-143">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="b02e3-144">**UninstallLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b02e3-144">**UninstallLicenseKeyPack**</span></span>](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | <span data-ttu-id="b02e3-145">Disinstalla un Key Pack per le licenze Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b02e3-145">Uninstalls a Remote Desktop Services license key pack.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="b02e3-146">**UninstallLicenseKeyPackWithId**</span><span class="sxs-lookup"><span data-stu-id="b02e3-146">**UninstallLicenseKeyPackWithId**</span></span>](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | <span data-ttu-id="b02e3-147">Disinstalla il Key Pack di Servizi Desktop remoto License con l'identificatore del Key Pack specificato.</span><span class="sxs-lookup"><span data-stu-id="b02e3-147">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="b02e3-148">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b02e3-148">Properties</span></span>

<span data-ttu-id="b02e3-149">La classe **Win32 \_ TSLicenseKeyPack** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b02e3-149">The **Win32\_TSLicenseKeyPack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b02e3-150">**AccessRights**</span><span class="sxs-lookup"><span data-stu-id="b02e3-150">**AccessRights**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-153">Qualificatori: [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("sessione Desktop remoto", "VDI Session", "Calista", "VDI Partners")</span><span class="sxs-lookup"><span data-stu-id="b02e3-153">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("RD Session", "VDI Session", "Calista", "VDI Partners")</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-154">Qualificatore per i diritti di accesso del key pack licenze Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="b02e3-154">Qualifier for TS Licensing key pack access rights</span></span>

</dd> <dt>

<span data-ttu-id="b02e3-155">**AvailableLicenses**</span><span class="sxs-lookup"><span data-stu-id="b02e3-155">**AvailableLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-156">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-158">Numero totale di licenze disponibili nel Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-158">Total number of available licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="b02e3-159">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b02e3-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b02e3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-162">Descrizione del Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-162">Description of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="b02e3-163">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="b02e3-163">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-164">Tipo di dati: **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="b02e3-164">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-166">Data di scadenza del Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-166">The expiration date of the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="b02e3-167">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="b02e3-167">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-170">Numero totale di licenze rilasciate nel Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-170">Total number of issued licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="b02e3-171">**KeyPackId**</span><span class="sxs-lookup"><span data-stu-id="b02e3-171">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-174">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b02e3-174">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-175">Identificatore per il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-175">Identifier for the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="b02e3-176">**KeyPackType**</span><span class="sxs-lookup"><span data-stu-id="b02e3-176">**KeyPackType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-177">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-179">Tipo di Key Pack per il server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b02e3-179">Type of key pack for the Remote Desktop license server.</span></span>

| <span data-ttu-id="b02e3-180">Valore</span><span class="sxs-lookup"><span data-stu-id="b02e3-180">Value</span></span> | <span data-ttu-id="b02e3-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b02e3-181">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="b02e3-182">0</span><span class="sxs-lookup"><span data-stu-id="b02e3-182">0</span></span> | <span data-ttu-id="b02e3-183">Il tipo di Key Pack del Servizi Desktop remoto License è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b02e3-183">The Remote Desktop Services license key pack type is unknown.</span></span> |
| <span data-ttu-id="b02e3-184">1</span><span class="sxs-lookup"><span data-stu-id="b02e3-184">1</span></span> | <span data-ttu-id="b02e3-185">Il tipo di Key Pack per le licenze Servizi Desktop remoto è un acquisto al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="b02e3-185">The Remote Desktop Services license key pack type is a retail purchase.</span></span> |
| <span data-ttu-id="b02e3-186">2</span><span class="sxs-lookup"><span data-stu-id="b02e3-186">2</span></span> | <span data-ttu-id="b02e3-187">Il tipo di Key Pack del Servizi Desktop remoto License è un Volume Purchase.</span><span class="sxs-lookup"><span data-stu-id="b02e3-187">The Remote Desktop Services license key pack type is a volume purchase.</span></span> |
| <span data-ttu-id="b02e3-188">3</span><span class="sxs-lookup"><span data-stu-id="b02e3-188">3</span></span> | <span data-ttu-id="b02e3-189">Il tipo di Key Pack del Servizi Desktop remoto License è una licenza simultanea.</span><span class="sxs-lookup"><span data-stu-id="b02e3-189">The Remote Desktop Services license key pack type is a concurrent license.</span></span> |
| <span data-ttu-id="b02e3-190">4</span><span class="sxs-lookup"><span data-stu-id="b02e3-190">4</span></span> | <span data-ttu-id="b02e3-191">Il tipo di Key Pack del Servizi Desktop remoto License è temporaneo.</span><span class="sxs-lookup"><span data-stu-id="b02e3-191">The Remote Desktop Services license key pack type is temporary.</span></span> |
| <span data-ttu-id="b02e3-192">5</span><span class="sxs-lookup"><span data-stu-id="b02e3-192">5</span></span> | <span data-ttu-id="b02e3-193">Il tipo di Key Pack del Servizi Desktop remoto License è una licenza Open.</span><span class="sxs-lookup"><span data-stu-id="b02e3-193">The Remote Desktop Services license key pack type is an open license.</span></span> |
| <span data-ttu-id="b02e3-194">6</span><span class="sxs-lookup"><span data-stu-id="b02e3-194">6</span></span> | <span data-ttu-id="b02e3-195">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="b02e3-195">Not supported.</span></span> |

<span data-ttu-id="b02e3-196">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="b02e3-196">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-197">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-199">Tipo di prodotto del Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-199">Product type of the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="b02e3-200">Valore</span><span class="sxs-lookup"><span data-stu-id="b02e3-200">Value</span></span> | <span data-ttu-id="b02e3-201">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b02e3-201">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="b02e3-202">0</span><span class="sxs-lookup"><span data-stu-id="b02e3-202">0</span></span> | <span data-ttu-id="b02e3-203">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b02e3-203">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="b02e3-204">Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="b02e3-204">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="b02e3-205">1</span><span class="sxs-lookup"><span data-stu-id="b02e3-205">1</span></span> | <span data-ttu-id="b02e3-206">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente.</span><span class="sxs-lookup"><span data-stu-id="b02e3-206">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="b02e3-207">Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="b02e3-207">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="b02e3-208">2</span><span class="sxs-lookup"><span data-stu-id="b02e3-208">2</span></span> | <span data-ttu-id="b02e3-209">Questo tipo di prodotto non è valido.</span><span class="sxs-lookup"><span data-stu-id="b02e3-209">This product type is not valid.</span></span> |

<span data-ttu-id="b02e3-210">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="b02e3-210">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b02e3-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-213">Versione del prodotto per il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-213">Product version for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="b02e3-214">Valore</span><span class="sxs-lookup"><span data-stu-id="b02e3-214">Value</span></span> | <span data-ttu-id="b02e3-215">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b02e3-215">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="b02e3-216">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="b02e3-216">"Windows Server 2012"</span></span> | <span data-ttu-id="b02e3-217">Con questa licenza sono supportati solo i server che eseguono Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b02e3-217">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="b02e3-218">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="b02e3-218">"Windows Server 7"</span></span> | <span data-ttu-id="b02e3-219">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b02e3-219">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span> |
| <span data-ttu-id="b02e3-220">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="b02e3-220">"Windows Server 2008"</span></span> | <span data-ttu-id="b02e3-221">Questo Key Pack supporta solo i server che eseguono Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b02e3-221">Only servers running Windows Server 2008 are supported by this key pack.</span></span> |

<span data-ttu-id="b02e3-222">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="b02e3-222">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-223">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-225">Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-225">Product version identifier for the Remote Desktop Services license key pack.</span></span>

| <span data-ttu-id="b02e3-226">Valore</span><span class="sxs-lookup"><span data-stu-id="b02e3-226">Value</span></span> | <span data-ttu-id="b02e3-227">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b02e3-227">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="b02e3-228">0</span><span class="sxs-lookup"><span data-stu-id="b02e3-228">0</span></span> | <span data-ttu-id="b02e3-229">Non supportato</span><span class="sxs-lookup"><span data-stu-id="b02e3-229">Not supported</span></span> |
| <span data-ttu-id="b02e3-230">1</span><span class="sxs-lookup"><span data-stu-id="b02e3-230">1</span></span> | <span data-ttu-id="b02e3-231">Non supportato</span><span class="sxs-lookup"><span data-stu-id="b02e3-231">Not supported</span></span> |
| <span data-ttu-id="b02e3-232">2</span><span class="sxs-lookup"><span data-stu-id="b02e3-232">2</span></span> | <span data-ttu-id="b02e3-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b02e3-233">Windows Server 2008</span></span> |
| <span data-ttu-id="b02e3-234">3</span><span class="sxs-lookup"><span data-stu-id="b02e3-234">3</span></span> | <span data-ttu-id="b02e3-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b02e3-235">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="b02e3-236">4</span><span class="sxs-lookup"><span data-stu-id="b02e3-236">4</span></span> | <span data-ttu-id="b02e3-237">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b02e3-237">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="b02e3-238">5</span><span class="sxs-lookup"><span data-stu-id="b02e3-238">5</span></span> | <span data-ttu-id="b02e3-239">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b02e3-239">Windows Server 2016</span></span> |
| <span data-ttu-id="b02e3-240">6</span><span class="sxs-lookup"><span data-stu-id="b02e3-240">6</span></span> | <span data-ttu-id="b02e3-241">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="b02e3-241">Windows Server 2019</span></span> |

<span data-ttu-id="b02e3-242">**TotalLicenses**</span><span class="sxs-lookup"><span data-stu-id="b02e3-242">**TotalLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-243">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-245">Numero totale di licenze nel Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b02e3-245">Total number of licenses in the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="b02e3-246">**TypeAndModel**</span><span class="sxs-lookup"><span data-stu-id="b02e3-246">**TypeAndModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b02e3-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b02e3-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b02e3-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b02e3-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b02e3-249">Qualificatore per il tipo e il modello del Key Pack per licenze Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="b02e3-249">Qualifier for TS Licensing key pack type and model.</span></span> <span data-ttu-id="b02e3-250">Esempi: licenza di sottoscrizione per ogni dispositivo di VDI, licenza CAL per utente di Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="b02e3-250">Examples: VDI Per Device subscription license, TS Per User CAL</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b02e3-251">Commenti</span><span class="sxs-lookup"><span data-stu-id="b02e3-251">Remarks</span></span>

<span data-ttu-id="b02e3-252">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="b02e3-252">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="b02e3-253">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b02e3-253">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b02e3-254">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b02e3-254">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b02e3-255">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b02e3-255">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b02e3-256">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b02e3-256">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b02e3-257">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b02e3-257">Requirements</span></span>



| <span data-ttu-id="b02e3-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="b02e3-258">Requirement</span></span> | <span data-ttu-id="b02e3-259">Valore</span><span class="sxs-lookup"><span data-stu-id="b02e3-259">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02e3-260">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b02e3-260">Minimum supported client</span></span><br/> | <span data-ttu-id="b02e3-261">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b02e3-261">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b02e3-262">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b02e3-262">Minimum supported server</span></span><br/> | <span data-ttu-id="b02e3-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b02e3-263">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b02e3-264">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b02e3-264">Namespace</span></span><br/>                | <span data-ttu-id="b02e3-265">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b02e3-265">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b02e3-266">MOF</span><span class="sxs-lookup"><span data-stu-id="b02e3-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b02e3-267"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b02e3-267"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b02e3-268">DLL</span><span class="sxs-lookup"><span data-stu-id="b02e3-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b02e3-269"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b02e3-269"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b02e3-270">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b02e3-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02e3-271">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-271">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="b02e3-272">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-272">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="b02e3-273">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-273">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="b02e3-274">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b02e3-274">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

