---
description: Rappresenta una raccolta che fornisce funzionalità di elaborazione ed è costituita da \_ oggetti MANAGEDSYSTEMELEMENT CIM.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: Classe CIM_ComputerSystem (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319058"
---
# <a name="cim_computersystem-class-hyper-v-management"></a><span data-ttu-id="76196-103">Classe CIM_ComputerSystem (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="76196-103">CIM_ComputerSystem class (Hyper-V management)</span></span>

<span data-ttu-id="76196-104">Rappresenta una raccolta che fornisce funzionalità di elaborazione ed è costituita da oggetti [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="76196-104">Represents a collection that provides computing capabilities and consists of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="76196-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76196-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="76196-106">Members</span><span class="sxs-lookup"><span data-stu-id="76196-106">Members</span></span>

<span data-ttu-id="76196-107">La classe **CIM \_ ComputerSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="76196-107">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="76196-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="76196-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="76196-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76196-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="76196-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="76196-110">Methods</span></span>

<span data-ttu-id="76196-111">La classe **CIM \_ ComputerSystem** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="76196-111">The **CIM\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="76196-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="76196-112">Method</span></span>                                                    | <span data-ttu-id="76196-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76196-113">Description</span></span>                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76196-114">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="76196-114">**SetPowerState**</span></span>](cim-computersystem-setpowerstate.md) | <span data-ttu-id="76196-115">Questo metodo è deprecato.</span><span class="sxs-lookup"><span data-stu-id="76196-115">This method is deprecated.</span></span> <span data-ttu-id="76196-116">Usare invece il metodo **RequestPowerStateChange** nella classe **CIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="76196-116">Instead, use the **RequestPowerStateChange** method in the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="76196-117">**Descrizione deprecata:** Imposta lo stato di alimentazione del computer.</span><span class="sxs-lookup"><span data-stu-id="76196-117">**Deprecated description:** Sets the power state of the computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="76196-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76196-118">Properties</span></span>

<span data-ttu-id="76196-119">La classe **CIM \_ ComputerSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="76196-119">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76196-120">**Dedicato**</span><span class="sxs-lookup"><span data-stu-id="76196-120">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76196-121">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76196-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76196-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76196-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76196-123">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysServices "," FC-GS. INCIs-T11 \| Platform \| PlatformType "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**OtherDedicatedDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="76196-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.sysServices", "FC-GS.INCITS-T11 \| Platform \| PlatformType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**OtherDedicatedDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="76196-124">Lo scopo e le funzionalità del sistema informatico.</span><span class="sxs-lookup"><span data-stu-id="76196-124">The purpose and features of the computer system.</span></span> <span data-ttu-id="76196-125">Ad esempio, un sistema dedicato alla stampa potrebbe specificare "11" (Print).</span><span class="sxs-lookup"><span data-stu-id="76196-125">For example, a system dedicated to printing could specify "11" (Print).</span></span> <span data-ttu-id="76196-126">Un sistema di utilizzo generico con funzionalità di stampa può essere impostato su "0" (non dedicato) e "11" (Print).</span><span class="sxs-lookup"><span data-stu-id="76196-126">A general purpose system with printing capabilities can be set to "0" (Not Dedicated) and "11" (Print).</span></span>

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span data-ttu-id="76196-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Non dedicato** (0)</span><span class="sxs-lookup"><span data-stu-id="76196-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Not Dedicated** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76196-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (1)</span><span class="sxs-lookup"><span data-stu-id="76196-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76196-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (2)</span><span class="sxs-lookup"><span data-stu-id="76196-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="76196-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Archiviazione** (3)</span><span class="sxs-lookup"><span data-stu-id="76196-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span data-ttu-id="76196-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span><span class="sxs-lookup"><span data-stu-id="76196-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="76196-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span><span class="sxs-lookup"><span data-stu-id="76196-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span data-ttu-id="76196-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Switch di livello 3** (6)</span><span class="sxs-lookup"><span data-stu-id="76196-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3 Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span data-ttu-id="76196-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Switch ufficio centrale** (7)</span><span class="sxs-lookup"><span data-stu-id="76196-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Central Office Switch** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span data-ttu-id="76196-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span><span class="sxs-lookup"><span data-stu-id="76196-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span data-ttu-id="76196-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Server di accesso** (9)</span><span class="sxs-lookup"><span data-stu-id="76196-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Access Server** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span data-ttu-id="76196-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span><span class="sxs-lookup"><span data-stu-id="76196-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="76196-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Stampa** (11)</span><span class="sxs-lookup"><span data-stu-id="76196-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Print** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span data-ttu-id="76196-139"><span id="I_O"></span><span id="i_o"></span>**I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="76196-139"><span id="I_O"></span><span id="i_o"></span>**I/O** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span data-ttu-id="76196-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Caching Web** (13)</span><span class="sxs-lookup"><span data-stu-id="76196-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Web Caching** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span data-ttu-id="76196-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Gestione** (14)</span><span class="sxs-lookup"><span data-stu-id="76196-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Management** (14)</span></span>


</dt> <dd>

<span data-ttu-id="76196-142">Questa istanza è dedicata all'hosting del software di gestione del sistema</span><span class="sxs-lookup"><span data-stu-id="76196-142">This instance is dedicated to hosting system management software</span></span>

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span data-ttu-id="76196-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Blocca server** (15)</span><span class="sxs-lookup"><span data-stu-id="76196-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span data-ttu-id="76196-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File server** (16)</span><span class="sxs-lookup"><span data-stu-id="76196-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File Server** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span data-ttu-id="76196-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Dispositivo utente mobile** (17)</span><span class="sxs-lookup"><span data-stu-id="76196-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobile User Device** (17)</span></span>


</dt> <dd>

<span data-ttu-id="76196-146">Un esempio di dispositivo utente dedicato è un telefono cellulare o uno scanner di codice a barre in un negozio che comunica tramite frequenza radio.</span><span class="sxs-lookup"><span data-stu-id="76196-146">An example of a dedicated user device is a mobile phone or a barcode scanner in a store that communicates via radio frequency.</span></span> <span data-ttu-id="76196-147">Questi sistemi sono molto limitati in funzionalità e programmabilità e non sono considerati piattaforme di elaborazione "per utilizzo generico".</span><span class="sxs-lookup"><span data-stu-id="76196-147">These systems are quite limited in functionality and programmability, and are not considered 'general purpose' computing platforms.</span></span> <span data-ttu-id="76196-148">In alternativa, un esempio di sistema mobile che è "utilizzo generico" (ad esempio, non è dedicato) è un computer portatile.</span><span class="sxs-lookup"><span data-stu-id="76196-148">Alternately, an example of a mobile system that is 'general purpose' (i.e., is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="76196-149">Sebbene sia limitato nella programmabilità, è possibile scaricare il nuovo software e la relativa funzionalità espanso dall'utente.</span><span class="sxs-lookup"><span data-stu-id="76196-149">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span>

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span data-ttu-id="76196-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Ripetitore** (18)</span><span class="sxs-lookup"><span data-stu-id="76196-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span data-ttu-id="76196-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span><span class="sxs-lookup"><span data-stu-id="76196-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span data-ttu-id="76196-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span><span class="sxs-lookup"><span data-stu-id="76196-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span data-ttu-id="76196-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Virtualizzatore di archiviazione** (21)</span><span class="sxs-lookup"><span data-stu-id="76196-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Storage Virtualizer** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span data-ttu-id="76196-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Catalogo multimediale** (22)</span><span class="sxs-lookup"><span data-stu-id="76196-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Media Library** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span data-ttu-id="76196-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span><span class="sxs-lookup"><span data-stu-id="76196-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span data-ttu-id="76196-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**Testa NAS** (24)</span><span class="sxs-lookup"><span data-stu-id="76196-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS Head** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span data-ttu-id="76196-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**NAS autonomo** (25)</span><span class="sxs-lookup"><span data-stu-id="76196-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Self-contained NAS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span data-ttu-id="76196-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span><span class="sxs-lookup"><span data-stu-id="76196-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span data-ttu-id="76196-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**Telefono IP** (27)</span><span class="sxs-lookup"><span data-stu-id="76196-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP Phone** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span data-ttu-id="76196-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Controller di gestione** (28)</span><span class="sxs-lookup"><span data-stu-id="76196-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Management Controller** (28)</span></span>


</dt> <dd>

<span data-ttu-id="76196-161">Questa istanza rappresenta hardware specializzato dedicato alla gestione dei sistemi, ad esempio un controller di gestione (BMC) o un processore di servizi di battiscopa.</span><span class="sxs-lookup"><span data-stu-id="76196-161">This instance represents specialized hardware dedicated to systems management (i.e., a Baseboard Management Controller (BMC) or service processor).</span></span>

<span data-ttu-id="76196-162">L'ambito di gestione di un "controller di gestione" è in genere un singolo sistema gestito in cui è contenuto.</span><span class="sxs-lookup"><span data-stu-id="76196-162">The management scope of a "Management Controller" is typically a single managed system in which it is contained.</span></span>

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span data-ttu-id="76196-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Gestione chassis** (29)</span><span class="sxs-lookup"><span data-stu-id="76196-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis Manager** (29)</span></span>


</dt> <dd>

<span data-ttu-id="76196-164">Questa istanza rappresenta un sistema dedicato alla gestione di uno chassis del pannello e dei relativi dispositivi contenuti.</span><span class="sxs-lookup"><span data-stu-id="76196-164">This instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="76196-165">Questo valore verrebbe utilizzato per rappresentare un controller di scaffale.</span><span class="sxs-lookup"><span data-stu-id="76196-165">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="76196-166">Un "gestore dello chassis" è un punto di aggregazione per la gestione e può basarsi su controller di gestione subordinati per la gestione delle parti costituenti.</span><span class="sxs-lookup"><span data-stu-id="76196-166">A "Chassis Manager" is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span>

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span data-ttu-id="76196-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Controller RAID basato su host** (30)</span><span class="sxs-lookup"><span data-stu-id="76196-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host-based RAID controller** (30)</span></span>


</dt> <dd>

<span data-ttu-id="76196-168">Questa istanza rappresenta un controller di archiviazione RAID contenuto in un computer host.</span><span class="sxs-lookup"><span data-stu-id="76196-168">This instance represents a RAID storage controller contained within a host computer.</span></span>

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span data-ttu-id="76196-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Enclosure dispositivi di archiviazione** (31)</span><span class="sxs-lookup"><span data-stu-id="76196-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Storage Device Enclosure** (31)</span></span>


</dt> <dd>

<span data-ttu-id="76196-170">Questa istanza rappresenta un'enclosure che contiene dispositivi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76196-170">This instance represents an enclosure that contains storage devices.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="76196-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span><span class="sxs-lookup"><span data-stu-id="76196-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="76196-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Portatile** (33)</span><span class="sxs-lookup"><span data-stu-id="76196-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span data-ttu-id="76196-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Libreria di nastri virtuale** (34)</span><span class="sxs-lookup"><span data-stu-id="76196-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Virtual Tape Library** (34)</span></span>


</dt> <dd>

<span data-ttu-id="76196-174">Emulazione di una libreria di nastri da parte di un sistema di libreria virtuale.</span><span class="sxs-lookup"><span data-stu-id="76196-174">The emulation of a tape library by a Virtual Library System.</span></span>

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span data-ttu-id="76196-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Sistema di libreria virtuale** (35)</span><span class="sxs-lookup"><span data-stu-id="76196-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtual Library System** (35)</span></span>


</dt> <dd>

<span data-ttu-id="76196-176">Usa l'archiviazione su disco per emulare le librerie di nastri</span><span class="sxs-lookup"><span data-stu-id="76196-176">Uses disk storage to emulate tape libraries</span></span>

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span data-ttu-id="76196-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**PC di rete/thin client** (36)</span><span class="sxs-lookup"><span data-stu-id="76196-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Network PC/Thin Client** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span data-ttu-id="76196-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**Switch FC** (37)</span><span class="sxs-lookup"><span data-stu-id="76196-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC Switch** (37)</span></span>


</dt> <dd>

<span data-ttu-id="76196-179">Dedicato al cambio di frame Fibre Channel di livello 2.</span><span class="sxs-lookup"><span data-stu-id="76196-179">Dedicated to switching layer 2 fibre channel frames.</span></span>

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span data-ttu-id="76196-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Switch Ethernet** (38)</span><span class="sxs-lookup"><span data-stu-id="76196-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet Switch** (38)</span></span>


</dt> <dd>

<span data-ttu-id="76196-181">Dedicato al cambio di frame Ethernet di livello 2</span><span class="sxs-lookup"><span data-stu-id="76196-181">Dedicated to switching layer 2 ethernet frames</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="76196-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="76196-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="76196-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32568.. 65535)</span><span class="sxs-lookup"><span data-stu-id="76196-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32568..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76196-184">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="76196-184">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76196-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76196-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76196-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76196-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76196-187">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="76196-187">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="76196-188">Formato del nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="76196-188">The format of the computer system name.</span></span>

<dt>



 <span data-ttu-id="76196-189">("Altro")</span><span class="sxs-lookup"><span data-stu-id="76196-189">("Other")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-190">("IP")</span><span class="sxs-lookup"><span data-stu-id="76196-190">("IP")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-191">("Dial")</span><span class="sxs-lookup"><span data-stu-id="76196-191">("Dial")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-192">("HID")</span><span class="sxs-lookup"><span data-stu-id="76196-192">("HID")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-193">("NWA")</span><span class="sxs-lookup"><span data-stu-id="76196-193">("NWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-194">("HWA")</span><span class="sxs-lookup"><span data-stu-id="76196-194">("HWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-195">("X25")</span><span class="sxs-lookup"><span data-stu-id="76196-195">("X25")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-196">("ISDN")</span><span class="sxs-lookup"><span data-stu-id="76196-196">("ISDN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-197">("IPX")</span><span class="sxs-lookup"><span data-stu-id="76196-197">("IPX")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-198">("DCC")</span><span class="sxs-lookup"><span data-stu-id="76196-198">("DCC")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-199">("ICD")</span><span class="sxs-lookup"><span data-stu-id="76196-199">("ICD")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-200">("E. 164")</span><span class="sxs-lookup"><span data-stu-id="76196-200">("E.164")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-201">("SNA")</span><span class="sxs-lookup"><span data-stu-id="76196-201">("SNA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-202">("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="76196-202">("OID/OSI")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-203">("WWN")</span><span class="sxs-lookup"><span data-stu-id="76196-203">("WWN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="76196-204">("NAA")</span><span class="sxs-lookup"><span data-stu-id="76196-204">("NAA")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76196-205">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="76196-205">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76196-206">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="76196-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76196-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76196-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76196-208">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**Dedicato**")</span><span class="sxs-lookup"><span data-stu-id="76196-208">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**Dedicated**")</span></span>
</dt> </dl>

<span data-ttu-id="76196-209">Viene descritto come o perché il sistema è dedicato quando la matrice **dedicata** include il valore 2 (other).</span><span class="sxs-lookup"><span data-stu-id="76196-209">Describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="76196-210">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="76196-210">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76196-211">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76196-211">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76196-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76196-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76196-213">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controlli di alimentazione del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="76196-213">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="76196-214">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="76196-214">This property is deprecated.</span></span> <span data-ttu-id="76196-215">Usare invece il metodo **PowerChangeCapabilities** nella classe **CIM \_ PowerManagementCapabilitiesCIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="76196-215">Instead, use the **PowerChangeCapabilities** method in the **CIM\_PowerManagementCapabilitiesCIM\_PowerManagementService** class.</span></span>

<span data-ttu-id="76196-216">**Descrizione deprecata:** Funzionalità di risparmio energia del sistema.</span><span class="sxs-lookup"><span data-stu-id="76196-216">**Deprecated description:** The power management capabilities of the system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76196-217">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="76196-217">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="76196-218">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="76196-218">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="76196-219">**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="76196-219">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="76196-220">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="76196-220">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="76196-221">**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="76196-221">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="76196-222">**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="76196-222">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="76196-223">**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="76196-223">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="76196-224">**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="76196-224">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="76196-225">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="76196-225">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76196-226">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76196-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76196-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76196-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76196-228">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sicurezza hardware del sistema DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="76196-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="76196-229">Indica se il sistema supporta l'operazione di reimpostazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="76196-229">Indicates whether the system supports the hardware reset operation.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="76196-230">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="76196-230">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="76196-231">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="76196-231">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="76196-232">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="76196-232">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="76196-233">**Abilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="76196-233">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="76196-234">**Non implementato** (5)</span><span class="sxs-lookup"><span data-stu-id="76196-234">**Not Implemented** (5)</span></span>


<span data-ttu-id="76196-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="76196-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="76196-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76196-236">Requirements</span></span>



| <span data-ttu-id="76196-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="76196-237">Requirement</span></span> | <span data-ttu-id="76196-238">Valore</span><span class="sxs-lookup"><span data-stu-id="76196-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76196-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76196-239">Minimum supported client</span></span><br/> | <span data-ttu-id="76196-240">Windows 8</span><span class="sxs-lookup"><span data-stu-id="76196-240">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="76196-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76196-241">Minimum supported server</span></span><br/> | <span data-ttu-id="76196-242">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76196-242">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="76196-243">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76196-243">Namespace</span></span><br/>                | <span data-ttu-id="76196-244">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="76196-244">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="76196-245">MOF</span><span class="sxs-lookup"><span data-stu-id="76196-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76196-246"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76196-246"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76196-247">DLL</span><span class="sxs-lookup"><span data-stu-id="76196-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76196-248"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76196-248"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76196-249">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76196-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76196-250">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="76196-250">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

