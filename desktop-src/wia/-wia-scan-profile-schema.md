---
description: Lo schema del profilo di analisi definisce un formato XML che può essere utilizzato per archiviare le proprietà degli elementi di acquisizione immagini Windows (WIA), ad esempio scanner e fotocamere.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Schema del profilo di analisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307339"
---
# <a name="scan-profile-schema"></a><span data-ttu-id="891e9-103">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="891e9-103">Scan Profile Schema</span></span>

<span data-ttu-id="891e9-104">Lo schema del profilo di analisi definisce un formato XML che può essere utilizzato per archiviare le proprietà degli elementi di acquisizione immagini Windows (WIA), ad esempio scanner e fotocamere.</span><span class="sxs-lookup"><span data-stu-id="891e9-104">The Scan Profile Schema defines an XML format that can be used to store the properties of Windows Image Acquisition (WIA) items, such as scanners and cameras.</span></span> <span data-ttu-id="891e9-105">Questi file permanenti consentono alle applicazioni di fornire analisi automatica senza richiedere agli utenti di ricordare le impostazioni delle proprietà degli elementi.</span><span class="sxs-lookup"><span data-stu-id="891e9-105">These persistent files enable applications to provide automatic scanning without requiring users to remember the property settings of the items.</span></span>

<span data-ttu-id="891e9-106">Qualsiasi dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) può avere un profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="891e9-106">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="891e9-107">Tuttavia, gli elementi di **IWiaItem2** di tipo WIA \_ Category \_ finished \_ file e WIA \_ Category \_ root non possono avere profili.</span><span class="sxs-lookup"><span data-stu-id="891e9-107">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="891e9-108">I profili di analisi vengono creati e gestiti tramite le interfacce [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)e [**IScanProfileUI**](-wia-iscanprofileui.md) .</span><span class="sxs-lookup"><span data-stu-id="891e9-108">Scan profiles are created and managed through the [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md), and [**IScanProfileUI**](-wia-iscanprofileui.md) interfaces.</span></span> <span data-ttu-id="891e9-109">Gli utenti dell'applicazione possono modificare i profili in modo limitato usando il metodo [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="891e9-109">Users of your application can modify profiles in limited ways using the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="891e9-110">Tutti i profili di analisi hanno gli elementi seguenti: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , e `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="891e9-110">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="891e9-111">Il profilo predefinito di un dispositivo contiene anche un `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="891e9-111">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="891e9-112">L'elemento `<ProfileGUID>` e l' `<DeviceID>` elemento non possono essere modificati dopo la creazione del profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="891e9-112">The `<ProfileGUID>` element and the `<DeviceID>` element cannot be changed after the scan profile is created.</span></span> <span data-ttu-id="891e9-113">`<ProfileName>`È possibile modificare i valori dell'elemento e dell' `<WiaItem>` elemento.</span><span class="sxs-lookup"><span data-stu-id="891e9-113">The values of the `<ProfileName>` element and the `<WiaItem>` element can be modified.</span></span> <span data-ttu-id="891e9-114">L' `<Default>` elemento può essere aggiunto o eliminato.</span><span class="sxs-lookup"><span data-stu-id="891e9-114">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="891e9-115">Questa operazione può essere eseguita a livello usando i metodi [**IScanProfile:: Sename**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr:: sedefault**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="891e9-115">This can be done programatically using the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="891e9-116">Queste proprietà possono anche essere modificate dagli utenti tramite il metodo [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="891e9-116">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="891e9-117">L' `<Properties>` elemento contiene `<Property>` elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="891e9-117">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="891e9-118">Usare questi elementi per aggiungere qualsiasi proprietà del dispositivo o elemento WIA al profilo.</span><span class="sxs-lookup"><span data-stu-id="891e9-118">Use these to add any WIA item or device property to the profile.</span></span> <span data-ttu-id="891e9-119">È anche possibile sviluppare una propria immagine acquisizione `<Property>` Children.</span><span class="sxs-lookup"><span data-stu-id="891e9-119">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="891e9-120">In questo modo lo schema del profilo di analisi diventa estendibile.</span><span class="sxs-lookup"><span data-stu-id="891e9-120">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="891e9-121">Per ulteriori informazioni sull'estensione dello schema, vedere [definizione di proprietà personalizzate](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="891e9-121">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

<span data-ttu-id="891e9-122">Di seguito è riportato lo schema completo del profilo di analisi.</span><span class="sxs-lookup"><span data-stu-id="891e9-122">Here is the complete Scan Profile Schema.</span></span> <span data-ttu-id="891e9-123">Segue un profilo di esempio.</span><span class="sxs-lookup"><span data-stu-id="891e9-123">A sample profile follows.</span></span>


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



<span data-ttu-id="891e9-124">Fare clic su **Mostra esempio** per visualizzare un profilo di esempio.</span><span class="sxs-lookup"><span data-stu-id="891e9-124">Click **Show Example** to see a sample profile.</span></span>


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a><span data-ttu-id="891e9-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="891e9-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="891e9-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="891e9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="891e9-127">**IScanProfile:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="891e9-127">**IScanProfile::GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[<span data-ttu-id="891e9-128">**IScanProfile:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="891e9-128">**IScanProfile::SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)
</dt> <dt>

<span data-ttu-id="891e9-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="891e9-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="891e9-130">Costanti della proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="891e9-130">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="891e9-131">Definizione di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="891e9-131">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



