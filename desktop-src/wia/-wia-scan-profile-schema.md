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
# <a name="scan-profile-schema"></a>Schema del profilo di analisi

Lo schema del profilo di analisi definisce un formato XML che può essere utilizzato per archiviare le proprietà degli elementi di acquisizione immagini Windows (WIA), ad esempio scanner e fotocamere. Questi file permanenti consentono alle applicazioni di fornire analisi automatica senza richiedere agli utenti di ricordare le impostazioni delle proprietà degli elementi.

Qualsiasi dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) può avere un profilo di analisi. Tuttavia, gli elementi di **IWiaItem2** di tipo WIA \_ Category \_ finished \_ file e WIA \_ Category \_ root non possono avere profili.

I profili di analisi vengono creati e gestiti tramite le interfacce [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)e [**IScanProfileUI**](-wia-iscanprofileui.md) . Gli utenti dell'applicazione possono modificare i profili in modo limitato usando il metodo [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

Tutti i profili di analisi hanno gli elementi seguenti: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , e `<Properties>` . Il profilo predefinito di un dispositivo contiene anche un `<Default>` elemento.

L'elemento `<ProfileGUID>` e l' `<DeviceID>` elemento non possono essere modificati dopo la creazione del profilo di analisi. `<ProfileName>`È possibile modificare i valori dell'elemento e dell' `<WiaItem>` elemento. L' `<Default>` elemento può essere aggiunto o eliminato. Questa operazione può essere eseguita a livello usando i metodi [**IScanProfile:: Sename**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr:: sedefault**](-wia-iscanprofilemgr-setdefault.md) . Queste proprietà possono anche essere modificate dagli utenti tramite il metodo [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

L' `<Properties>` elemento contiene `<Property>` elementi figlio. Usare questi elementi per aggiungere qualsiasi proprietà del dispositivo o elemento WIA al profilo. È anche possibile sviluppare una propria immagine acquisizione `<Property>` Children. In questo modo lo schema del profilo di analisi diventa estendibile. Per ulteriori informazioni sull'estensione dello schema, vedere [definizione di proprietà personalizzate](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).

Di seguito è riportato lo schema completo del profilo di analisi. Segue un profilo di esempio.


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



Fare clic su **Mostra esempio** per visualizzare un profilo di esempio.


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

[**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Costanti della proprietà WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definizione di proprietà personalizzate](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



