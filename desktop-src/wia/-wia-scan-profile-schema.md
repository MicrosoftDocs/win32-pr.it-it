---
description: Lo schema del profilo di analisi definisce un formato XML che può essere usato per archiviare le proprietà degli elementi wia (Image Acquisition) di Windows, ad esempio scanner e fotocamere.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Schema del profilo di analisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81091e75269206b6b3b5a89f86c6f92da5c1d2080d90382ac6af48c6d1cc32ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208017"
---
# <a name="scan-profile-schema"></a>Schema del profilo di analisi

Lo schema del profilo di analisi definisce un formato XML che può essere usato per archiviare le proprietà degli elementi wia (Image Acquisition) di Windows, ad esempio scanner e fotocamere. Questi file permanenti consentono alle applicazioni di fornire l'analisi automatica senza richiedere agli utenti di ricordare le impostazioni delle proprietà degli elementi.

Qualsiasi [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) può avere un profilo di analisi. Tuttavia, **gli elementi IWiaItem2** di tipo WIA \_ CATEGORY FINISHED FILE e \_ \_ WIA CATEGORY \_ ROOT non possono \_ avere profili.

I profili di analisi vengono creati e gestiti tramite [**le interfacce IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)e [**IScanProfileUI.**](-wia-iscanprofileui.md) Gli utenti dell'applicazione possono modificare i profili in modi limitati usando il [**metodo IScanProfileUI::ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

Tutti i profili di analisi hanno gli elementi seguenti: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` e `<Properties>` . Anche il profilo predefinito di un dispositivo ha un `<Default>` elemento .

`<ProfileGUID>`L'elemento e `<DeviceID>` l'elemento non possono essere modificati dopo la creazione del profilo di analisi. I valori `<ProfileName>` dell'elemento e `<WiaItem>` dell'elemento possono essere modificati. `<Default>`L'elemento può essere aggiunto o eliminato. Questa operazione può essere eseguita a livello di codice usando i metodi [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr::SetDefault.**](-wia-iscanprofilemgr-setdefault.md) Queste proprietà possono anche essere modificate dagli utenti tramite il [**metodo IScanProfileUI::ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

`<Properties>`L'elemento contiene `<Property>` elementi figlio. Usare questi elementi per aggiungere qualsiasi elemento WIA o proprietà del dispositivo al profilo. È anche possibile sviluppare un'immagine personalizzata per gli elementi `<Property>` figlio. In questo modo lo schema del profilo di analisi è estensibile. Per altre informazioni sull'estensione dello schema, vedere [Definizione](-wia-defining-custom-properties.md)di proprietà personalizzate, [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile::SetProperty.**](-wia-iscanprofile-setproperty.md)

Ecco lo schema completo del profilo di analisi. Segue un profilo di esempio.


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



Fare **clic su Mostra** esempio per visualizzare un profilo di esempio.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Costanti della proprietà WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definizione di proprietà personalizzate](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



